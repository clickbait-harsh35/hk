import numpy as np

# Get the number of rows and columns from the user
nr = int(input("Enter the number of rows: "))
nc = int(input("Enter the number of columns: "))

# Get the matrix entries from the user
entries = list(map(int, input("Enter the matrix entries (space-separated): ").split()))

# Create the matrix and reshape it
a = np.array(entries).reshape(nr, nc)

# Print the original matrix
print('Matrix:\n', a)
a_inv=np.linalg.inv(a)
trans_ainv=np.transpose(a_inv)
det_a=np.linalg.det(a)
cof_a=np.dot(trans_ainv,det_a)
print("the cofactor of a",'\n',cof_a)
print("the determinant of a",'\n',det_a)
adj_a=np.transpose(cof_a)
print("the adjoint of a",'\n',adj_a)

