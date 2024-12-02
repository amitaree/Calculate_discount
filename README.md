def calculate_discount(price, discount_percent):
  """Calculates the final price after applying a discount.

  Args:
    price: The original price of the item.
    discount_percent: The discount percentage as a decimal.

  Returns:
    The final price after applying the discount.
  """

  if discount_percent >= 0.2:
    return price * (1 - discount_percent)
  else:
    return price


def main():
  """Gets the original price and discount percentage from the user, and prints the final price."""

  price = float(input("Enter the original price of the item: "))
  discount_percent = float(input("Enter the discount percentage as a decimal (e.g., 0.2 for 20%): "))

  final_price = calculate_discount(price, discount_percent)

  if final_price < price:
    print(f"The final price after applying the discount is ${final_price:.2f}.")
  else:
    print("No discount was applied.")


if __name__ == "__main__":
  main()# Calculate_discount
