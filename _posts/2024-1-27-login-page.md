<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #F4F4F4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        form {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            color: #000; /* Set text color to black */
        }
        label {
            display: block;
            margin-bottom: 8px;
        }
        input {
            width: 100%;
            padding: 8px;
            margin-bottom: 16px;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #4CAF50;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <form id="loginForm">
        <label for="username">Username:</label>
        <input type="text" id="username" name="username" required>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
        <button type="submit">Login</button>
    </form>
    <form id="signupForm">
        <label for="newUsername">New Username:</label>
        <input type="text" id="newUsername" name="newUsername" required>
        <label for="newPassword">New Password:</label>
        <input type="password" id="newPassword" name="newPassword" required>
        <button type="submit">Sign Up</button>
    </form>
    <script>
const apiUrl = 'http://127.0.0.1:8086/api/login/'; // Replace with the actual API URL
        // Make an HTTP GET request to the API
fetch(apiUrl)
    .then(response => response.json()) // Parse the JSON response
    .then(data => {
        // Organize the data into a dictionary
        const organizedData = {
            Login_api: {
                url_prefix: '/api/login',
                LoginAPI: {
                    get: {
                        description: 'Retrieve all Logins from the database',
                        url: '/api/login',
                        method: 'GET',
                        data: data, // Include the retrieved data here
                        mode: "cors"
                    },
                },
            },
            LoginListAPI: {
                LoginListAPI: {
                    get: {
                        description: 'Retrieve all Logins from the database',
                        url: '/api/login',
                        method: 'GET',
                        data: data, // Include the retrieved data here
                        mode: "cors"
                    },
                },
            },
        };
        // Now, you have the organized data in the "organizedData" dictionary
        Data = organizedData.Login_api.LoginAPI.get.data; //data[id].Login_name, image whatever u may need
    });
</script>
</body>
</html>