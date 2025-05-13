def write_even_numbers(input_file, output_file):
    with open(input_file, 'r') as infile:
        numbers = list(map(int, infile.read().split()))
    even_numbers = [num for num in numbers if num % 2 == 0]
    total = sum(even_numbers)
    with open(output_file, 'w') as outfile:
        outfile.write(' '.join(map(str, even_numbers)) + '\n')
        outfile.write(str(total) + '\n')
    return total
input_file = 'input.txt'
output_file = 'output.txt'
total = write_even_numbers(input_file, output_file)
print(total)
