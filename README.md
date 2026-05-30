# Math Library Documentation


## 3D VECTOR
### Class vec3

|||
|-|-|
|x, y, z|variables|
|vec3()|constructor to initialize all variables to 0|
|vec3(x, y, z)|constructor to initialize all variables to the parameters of the method|
|vec3(v)|constructor that initializes the vector to the parameters of another vector|
|vec3 operator=(rhs)|operator overload for "=". copies another vector rhs|
|vec3 operator-()|operator overload for negative sign. switches the sign of the vector|
|vec3 operator+(rhs)|operator overload for "+". adds this vector to another vector|
|vec3 operator+=(rhs)|operator overload for "+=". adds this vector to another vector|
|vec3 operator-(rhs)|operator overload for "-". substracts another vector from this vector|
|vec3 operator-=(rhs)|operator overload for "-=". substracts another vector from this vector|
|vec3 operator*=(scalar)|operator overload for "*=". multiplies the vector by a scalar|
|vec3 operator*(scalar)|operator overload for "*". multiplies the vector by a scalar|
|bool operator==(rhs)|operator overload for "==". compares this vector to another vector. returns true if they are the same|
|bool operator!=(rhs)|operator overload for "!=". compares this vector to another vector. returns true if they are different|
|float operator\[](i)|operator overload for "[]". returns a copy of x, y or z, at the respective indexes 0, 1 or 2 for non-const vectors|
|const float operator\[](i)|operator overload for "[]". returns a reference to x, y or z, at the respective indexes 0, 1 or 2 for const vectors|


### Outside the class
|||
|-|-|
|float dot(a,b)|returns the dot product of two 3D vectors a and b|
|float length(v)|returns the length of a 3D vector v|
|vec3 cross(a,b)|returns the cross product of two 3D vectors a,b|
|vec3 normalize(v)|returns a normalized 3D vector v|



## 4D VECTOR
### Class vec4

|||
|-|-|
|x, y, z, w|variables|
|vec4()|constructor to initialize all variables to 0|
|vec4(x, y, z, w)|constructor to initialize all variables to the parameters of the method|
|vec4(v)|constructor that initializes the vector to the parameters of another vector|
|vec4 operator=(rhs)|operator overload for "=". copies another vector rhs|
|vec4 operator-()|operator overload for negative sign. switches the sign of the vector|
|vec4 operator+(rhs)|operator overload for "+". adds this vector to another vector|
|vec4 operator+=(rhs)|operator overload for "+=". adds this vector to another vector|
|vec4 operator-(rhs)|operator overload for "-". substracts another vector from this vector|
|vec4 operator-=(rhs)|operator overload for "-=". substracts another vector from this vector|
|vec4 operator*=(scalar)|operator overload for "*=". multiplies the vector by a scalar|
|vec4 operator*(scalar)|operator overload for "*". multiplies the vector by a scalar|
|bool operator==(rhs)|operator overload for "==". compares this vector to another vector. returns true if they are the same|
|bool operator!=(rhs)|operator overload for "!=". compares this vector to another vector. returns true if they are different|
|float operator\[](i)|operator overload for "[]". returns a copy of x, y, z or w, at the respective indexes 0, 1, 2 or 3 for non-const vectors|
|const float operator\[](i)|operator overload for "[]". returns a reference to x, y, z or w, at the respective indexes 0, 1, 2 or 3  for const vectors|


### Outside the class
|||
|-|-|
|float dot(a,b)|returns the dot product of two 4D vectors a and b|
|float length(v)|returns the length of a 4D vector v|
|vec4 normalize(v)|returns a normalized 4D vector v|


## 4D MATRIX
### Class mat4
|||
|-|-|
|vec4 m[4]|variable that stores a matrix|
|mat4()|creates an identity matrix|
|mat4(r0,r1,r2,r3)|creates a matrix from given 4D vectors r0, r1, r2 and r3|
|mat4(m)|duplicates a matrix m|
|mat4 operator=(rhs)|operator overload for "=". copies another matrix rhs|
|mat4 operator*(mat4& rhs)|operator overload for "*". multiplies the matrix by another matrix rhs|
|mat4 operator*(vec4& rhs)|operator overload for "*". multiplies the matrix by a 4D vector rhs|
|bool operator==(rhs)|operator overload for "==". compares this matrix to another. returns true if they match|
|bool operator!=(rhs)|operator overload for "!=". compares this matrix to another. returns true if they do not match|
|vec4 operator\[](i)|operator overload for "[]". returns a reference to a row in m at the index i (0-3)
|const vec4 operator\[](i)|operator overload for "[]". returns a const reference to a row in m at the index i (0-3)

### Outside the class
|||
|-|-|
|float determinant(m)|returns the determinant of a matrix m|
|mat4 inverse(m)|returns the inverse of a matrix m. if the matrix is not invertible, returns the identity matrix|
|mat4 transpose(m)|returns the transpose of a matrix m|
|mat4 rotationx(rad)|rotates a matrix around the X-axis given an angle rad in radians|
|mat4 rotationy(rad)|rotates a matrix around the Y-axis given an angle rad in radians|
|mat4 rotationz(rad)|rotates a matrix around the Z-axis given an angle rad in radians|
|mat4 rotationaxis(v, rad)|rotates a matrix around a 3D axis v given an angle rad in radians|