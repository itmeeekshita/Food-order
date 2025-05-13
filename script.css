let cart = [];
let total = 0;

function addToCart(itemName, itemPrice) {
  cart.push({ name: itemName, price: itemPrice });
  total += itemPrice;
  updateCart();
}

function removeFromCart(index) {
  total -= cart[index].price;
  cart.splice(index, 1);
  updateCart();
}

function updateCart() {
  const cartItems = document.getElementById("cart-items");
  cartItems.innerHTML = "";

  cart.forEach((item, index) => {
    const li = document.createElement("li");
    li.innerHTML = `
      ${item.name} - ₹${item.price}
      <button onclick="removeFromCart(${index})">Remove</button>
    `;
    cartItems.appendChild(li);
  });

  document.getElementById("total").innerText = `Total: ₹${total}`;
}

function placeOrder() {
  if (cart.length === 0) {
    alert("Your cart is empty!");
    return;
  }

  // Replace entire content with Thank You message
  document.getElementById("main-content").innerHTML = `
    <div class="thank-you">
      <h1>✅ Your Order is Placed!</h1>
      <p>Thank you for ordering. Your food will be delivered soon.</p>
    </div>
  `;
}
