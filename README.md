# Go Slice Sample

## Slice


## Code
```Go
func main() {
	// Slice generation
	tenSlice := make([]int, 10)
	fmt.Println(tenSlice)

	// Assignments to Elements
	tenSlice[0] = 123
	tenSlice[3] = 456
	tenSlice[6] = 789
	fmt.Println(tenSlice)

	// Value Reference
	fmt.Println(tenSlice[0])
	fmt.Println(tenSlice[1])

	// Number of elements in slice
	fmt.Println(len(tenSlice))

	// Slice Capacity
	fmt.Println(cap(tenSlice))

	// Simple Slice Expressions
	fiveSlice := tenSlice[2:7]
	fmt.Println(fiveSlice)

	// Element Extension
	elevenSlice := append(tenSlice, 101112)
	fmt.Println(elevenSlice)

	// Full Slice Expressions
	fullSlice := tenSlice[1:7:8]
	fmt.Println(fullSlice)

	// Output by for
	for i, s := range tenSlice {
		fmt.Println(strconv.Itoa(i) + " : " + strconv.Itoa(s))
	}
}
```

## Output Sample
~ $ go build slice.go  
~ $ ./slice  
[0 0 0 0 0 0 0 0 0 0]  
[123 0 0 456 0 0 789 0 0 0]  
123  
0  
10  
10  
[0 456 0 0 789]  
[123 0 0 456 0 0 789 0 0 0 101112]  
[0 0 456 0 0 789]  
0 : 123  
1 : 0  
2 : 0  
3 : 456  
4 : 0  
5 : 0  
6 : 789  
7 : 0  
8 : 0  
9 : 0  
