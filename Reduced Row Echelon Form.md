### Properties
- All nonzero rows are above any rows of all zeros
- Each leading entry of a row is in a column to the right of the leading entry of the row above it.
- All entries in a column below a leading entry are zeros.
- Leading entry in each non zero row is **1**.
- Each leading **1** is the only nonzero entry in it's column.

When converted to the reduced row echelon form:
The system of linear equations:
- Is **inconsistent (no solutions)** if the RREF has a pivot in the last column.
- Has a **unique solution** if RREF has a pivot in every column besides the last one/
- Has **many solutions** if the last column and at least one more column in the RREF do not have pivots. 
[[Every system of linear equations has either no sols...|Proof]]
### Additional terms
- Zero row - A row of a [[Augmented Matrix|matrix]] where every entry is 0.
- Leading one - The leftmost nonzero entry of any row that isn't a **zero row**. This leading one is called a **Pivot Position**.
- Pivot colum - A column containing a **Pivot position**.
