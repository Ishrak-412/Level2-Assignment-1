### Problem 1

Concept is default parameter(The default parameter is used when the argument is undefined).\
Function: multiplyValue(value: number, multiplier?: number): number


### Problem 2

Concept is Union type.\
Function: processInput(input: string | number | boolean): string | number

Returns a formatted result based on the input type:
string: trimmed and lowercased
number: multiplied by 10
boolean: "Active" for true, "Inactive" for false

### Problem 3

Concept is readonly tuple.\
Function: formatCoordinate(coordinate: readonly [number, number, string]): string

### Problem 4

Concept is rest parameter.\
Function: concatenateArrays<T>(...arrays: T[][]): T[]

### Problem 5

Concept is interface.\
Interface: Course with title (string), students (number), isPublished (boolean)

Function: getPopularCourses(courses: Course[], minStudents: number): Course[]

### Problem 6

Concepts is indexed access types.\
Function: pluckValues<T, K extends keyof T>(items: T[], key: K): T[K][]

### Problem 7

Concept is classes, inheritance, protected and private modifiers, super.\
Class: Employee

protected name: string
private baseSalary: number
getDetails() returns "Employee: [name], Base Salary: [baseSalary]"

Class: Manager extends Employee

private department: string
getRoleInfo() returns "Manager of [department]: [name]"

### Problem 8

Concept is async function, error handling.\
Function: validateAgeAsync(age: number): Promise<string>

If age >= 18: resolves with "Access Granted" after 1 second.
If age < 18: rejects immediately with new Error("Access Denied: Must be 18 or older").


### Blogs

[Type vs Interface]([type-vs-interface].md)\
[Access_Modifiers]([Access-modifiers].md)

