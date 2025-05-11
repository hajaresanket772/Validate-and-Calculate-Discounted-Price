# Validate-and-Calculate-Discounted-Price
function calculatePrice(price, discount = 10) {
  // Validate if the price is a valid positive number
  if (isNaN(price) || price <= 0) {
    console.error("Invalid price. Please provide a valid positive number.");
    return; // Exit the function if the price is invalid
  }

  // Validate if the discount is a valid positive number
  if (isNaN(discount) || discount < 0 || discount > 100) {
    console.error("Invalid discount. Please provide a valid discount percentage (0-100).");
    return; // Exit the function if the discount is invalid
  }

  // Calculate the final price after applying the discount
  let finalPrice = price - (price * (discount / 100));

  // Return the final price
  return finalPrice;
}

// Example usage:
let price = 100; // Example price
let discount = 15; // Example discount (you can try different values, or leave it empty for the default)
let finalPrice = calculatePrice(price, discount);

if (finalPrice) {
  console.log(`The final price after applying the discount is: $${finalPrice}`);
}

