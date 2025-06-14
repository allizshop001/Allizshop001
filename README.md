## Hi there 👋

<!--
**allizshop001/Allizshop001** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
*1. index.html*
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Alliz Shop</title>
  <style>
    body { font-family: Arial; padding: 20px; }
    .product { border: 1px solid #ccc; padding: 15px; margin-bottom: 20px; }
    #paypal-button-container { margin-top: 10px; }
  </style>
</head>
<body>
  <h1>Bienvenue sur Alliz Shop</h1>
  <div class="product">
    <h2>Produit : Casque Bluetooth</h2>
    <p>Prix : 50 $</p>
    <div id="paypal-button-container"></div>
  </div>

  <script src="https://www.paypal.com/sdk/js?client-id=alimukalay@gmail.com_ID&currency=USD"></script>
  <script>
    paypal.Buttons({
      createOrder: function(data, actions) {
        const price = 50;
        const total = price + (price * 0.10); // 10% de commission

        return actions.order.create({
          purchase_units: [{
            amount: { value: total.toFixed(2) }
          }]
        });
      },
      onApprove: function(data, actions) {
        return actions.order.capture().then(function(details) {
          alert('Paiement réussi par ' + details.payer.name.given_name);
        });
      }
    }).render('#paypal-button-container');
  </script>“`php
<?phpprix = 50;
commission =prix * 0.10;
montant_total =prix + commission;

echo "Prix :prix USD<br>";
echo "Commission (10%) : commission USD<br>";
echo "Montant total :montant_total USD<br>";
?>

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Paiement Airtel Money</title>
</head>
<body>
  <h2>Paiement via Airtel Money</h2>
  <form action="airtel_process.php" method="POST">
    <label>Nom complet :</label><br>
    <input type="text" name="nom" required><br><br>

    <label>Numéro Airtel (+243994901979):</label><br>
    <input type="text" name="numero" required><br><br>

    <label>Montant () :</label><br>
    <input type="number" name="montant" value="50" readonly><br><br>

    <input type="submit" value="Payer">
  </form>
</body>
</html>
“`
