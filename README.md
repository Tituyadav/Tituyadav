
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def main():
    while True:
        try:
            num = int(input("Enter a number (or 'q' to quit): "))
            if num == 'q':
                break
            if is_prime(num):
                print(num, "is a prime number.")
            else:
                print(num, "is not a prime number.")
        except ValueError:
            print("Invalid input. Please enter a valid number or 'q' to quit.")

if __name__ == "__main__":
    main()
