# lambda-mapping
def lambdaMap(arr):
    result = []
    for sublist in arr:
        # Filter out the elements less than or equal to 0
        filtered_sublist = list(filter(lambda x: x > 0, sublist))
        # Square each element in the filtered sublist
        squared_sublist = list(map(lambda x: x**2, filtered_sublist))
        result.append(squared_sublist)
    return result

# Read the input
n = int(input())
arr = []
for _ in range(n):
    sublist = list(map(int, input().split()))
    arr.append(sublist)

# Call the lambdaMap function
output = lambdaMap(arr)

# Print the output
for sublist in output:
    print(*sublist)




