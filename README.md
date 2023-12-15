# Loops
def calculate_interest(principle, rate):
    return principle * rate

def calculate_ending_balance(principle, interest):
    return principle + interest

def main():
    # User input for principal amount and interest rate
    principle = float(input("Enter principal amount: $"))
    rate = float(input("Enter interest rate (as a decimal): "))

    # Display header
    print("\nYear | Beginning Balance | Interest | Ending Balance")

    accumulated_interest = 0.0

    for year in range(1, 6):  # Loop for 5 years
        # Calculate annual interest and ending balance
        interest = calculate_interest(principle, rate)
        ending_balance = calculate_ending_balance(principle, interest)

        # Display results for the current year
        print(f"{year:<4} | {principle:18,.2f} | {interest:8,.2f} | {ending_balance:13,.2f}")

        # Update accumulated interest and set the new principle for the next year
        accumulated_interest += interest
        principle = ending_balance

    # Display accumulated interest for the 5 years
    print(f"\nAccumulated Interest for 5 Years: ${accumulated_interest:.2f}")

if __name__ == "__main__":
    main()
