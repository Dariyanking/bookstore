<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Book Store</title>
<style>
  /* Basic styling */
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-image: url('https://i0.wp.com/stanzaliving.wpcomstaging.com/wp-content/uploads/2023/07/Book-stores-in-Pune.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    color: #fff;
  }
  form {
    background-color: rgba(0, 0, 0, 0.7);
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    width: 300px;
  }
  input {
    margin-bottom: 10px;
    padding: 8px;
    width: 100%;
    box-sizing: border-box;
  }
  input[type="text"],
  input[type="email"],
  input[type="password"] {
    background-color: rgba(255, 255, 255, 0.8);
    border: none;
    color: #333;
  }
  input[type="submit"] {
    background-color: #007bff;
    color: #fff;
    cursor: pointer;
    border: none;
  }
  input[type="submit"]:hover {
    background-color: #0056b3;
  }
</style>
</head>
<body>
  <form id="signup-form" onsubmit="return validateForm()">
    <h2 style="text-align: center;">Sign Up</h2>
    <input type="text" id="name" placeholder="Name">
    <input type="email" id="email" placeholder="Email">
    <input type="password" id="password" placeholder="Password">
    <input type="submit" value="Sign Up">
  </form>

  <script>
    function validateForm() {
      var name = document.getElementById('name').value;
      var email = document.getElementById('email').value;
      var password = document.getElementById('password').value;

      // Basic validation
      if (name === '' || email === '' || password === '') {
        alert('Please fill in all fields.');
        return false;
      }

      // Email validation regex
      var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(email)) {
        alert('Please enter a valid email address.');
        return false;
      }

      // Password length validation
      if (password.length < 8) {
        alert('Password must be at least 8 characters long.');
        return false;
      }

      // If all validations pass, form submission is allowed
      return true;
    }
  </script>
</body>
</html>
