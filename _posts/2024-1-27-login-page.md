<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Information Form</title>
</head>
<body>
<h1>User Information Form</h1>
<form action="process_form.php" method="post" onsubmit="return redirectAndSubmit()">
    <!-- Username -->
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required>
    <br>
    <!-- Password -->
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>
    <br>
    <!-- Name -->
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    <br>
    <!-- Email -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <br>
    <br>
    <!-- Submit Button -->
    <input type="submit" value="Submit">
</form>

<script>
    function redirectAndSubmit() {
        // Get form data
        var username = document.getElementById('username').value;
        var password = document.getElementById('password').value;
        var name = document.getElementById('name').value;
        var email = document.getElementById('email').value;

        // Perform form data processing (e.g., send to PHP backend)
        // ...

        // Redirect to a specific link
        window.location.href = "http://127.0.0.1:4200/student2.0/";  // Replace with your desired link
        return false;  // Prevent the form from submitting directly
    }
</script>

</body>
</html>
