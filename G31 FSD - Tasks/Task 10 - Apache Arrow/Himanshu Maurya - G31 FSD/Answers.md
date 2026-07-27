
# Apache Arrow Assignment Solution

## Task 1

``` python
employee_table = pa.table(data)
```

## Task 2

Schema: - `employee_id` → `int64` - `name` → `string` - `salary` →
`int64`

## Task 3

-   Rows: `6`
-   Columns: `5`
-   Column names:
    -   employee_id
    -   name
    -   department
    -   salary
    -   city

``` python
print(employee_table.num_rows)
print(employee_table.num_columns)
print(employee_table.column_names)
print(employee_table.column("name"))
print(employee_table.slice(0, 3))
```

## Task 4

``` python
selected_table = employee_table.select(["name", "department", "salary"])
```

## Task 5

``` python
high_salary_table = employee_table.filter(
    pc.greater(employee_table["salary"], 50000)
)
```

Employees returned: Asha, Neha, Vikram, Arjun.

## Task 6

``` python
it_employees = employee_table.filter(
    pc.equal(employee_table["department"], "IT")
)
```

Employees returned: Asha, Neha.

## Task 7

-   Average salary: **57166.67**
-   Maximum salary: **70000**
-   Minimum salary: **45000**
-   Total salary: **343000**

## Task 8

``` python
bonus = pc.multiply(employee_table["salary"], 0.10)
employee_table = employee_table.append_column("bonus", bonus)
```

## Task 9

``` python
employee_df = employee_table.to_pandas()
```

## Task 10

``` python
new_arrow_table = pa.Table.from_pandas(employee_df, preserve_index=False)
```

## Task 11

``` python
pq.write_table(employee_table, "employees.parquet")
```

## Task 12

``` python
loaded_table = pq.read_table("employees.parquet")
```

## Task 13

``` python
with ipc.new_file("employees.arrow", employee_table.schema) as writer:
    writer.write_table(employee_table)
```

## Task 14

``` python
with ipc.open_file("employees.arrow") as reader:
    ipc_table = reader.read_all()
```

# Bonus Tasks

1.  Filter employees from Delhi.
2.  Filter salaries between 50000 and 65000.
3.  Add `annual_salary = salary * 12`.
4.  Save IT employees to `it_employees.parquet`.
5.  Read only `name` and `salary` columns.
6.  Sort by salary in descending order.

## Generated Files

-   apache_arrow_assignment.py
-   employees.parquet
-   employees.arrow
-   it_employees.parquet
