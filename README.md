<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Dubai Jackpot - Play, Win, and Enjoy!">
    <title>Dubai Jackpot</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        h1, h2, h3 {
            margin: 0;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
        }
        header {
            background-color: #ff5722;
            color: white;
            padding: 15px 0;
        }
        nav a {
            margin: 0 15px;
            color: white;
            text-decoration: none;
            font-weight: bold;
        }
        .section {
            padding: 50px 0;
        }
        .btn {
            background-color: #ff5722;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border: none;
            cursor: pointer;
            font-size: 1em;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #e64a19;
        }
        .auth-form {
            display: flex;
            flex-direction: column;
            max-width: 300px;
            margin: 20px auto;
        }
        .auth-form input {
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .auth-form button {
            background-color: #ff5722;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .auth-form button:hover {
            background-color: #e64a19;
        }
        #gameSection, #profileSection, #rechargeSection, #ticketHistorySection {
            display: none;
        }
        #ticketDisplay, #resultDisplay {
            margin-top: 20px;
            font-size: 1.5em;
            font-weight: bold;
            color: #ff5722;
        }
        #balanceDisplay, #withdrawDisplay {
            margin-top: 20px;
            font-size: 1.2em;
            color: #333;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1>Dubai Jackpot</h1>
            <nav>
                <a href="#signup">Sign Up</a>
                <a href="#login">Login</a>
                <a href="#gameSection">Play Lottery</a>
                <a href="#profileSection">Profile</a>
                <a href="#rechargeSection">Recharge</a>
                <a href="#ticketHistorySection">Ticket History</a>
            </nav>
        </div>
    </header>

    <!-- Sign-Up Section -->
    <section id="signup" class="section">
        <div class="container">
            <h2>Sign Up</h2>
            <form class="auth-form" id="signupForm">
                <input type="text" id="signupUsername" placeholder="Username" required>
                <input type="password" id="signupPassword" placeholder="Password" required>
                <input type="email" id="signupEmail" placeholder="Email" required>
                <input type="text" id="signupReferralCode" placeholder="Referral Code (Optional)">
                <button type="submit">Sign Up</button>
            </form>
            <p id="signupMessage"></p>
        </div>
    </section>

    <!-- Login Section -->
    <section id="login" class="section">
        <div class="container">
            <h2>Login</h2>
            <form class="auth-form" id="loginForm">
                <input type="text" id="loginUsername" placeholder="Username" required>
                <input type="password" id="loginPassword" placeholder="Password" required>
                <button type="submit">Login</button>
            </form>
            <p id="loginMessage"></p>
        </div>
    </section>

    <!-- Lottery Game Section -->
    <section id="gameSection" class="section">
        <div class="container">
            <h2>Welcome to Dubai Jackpot!</h2>
            <button class="btn" id="generateTicketBtn">Generate Lottery Ticket</button>
            <div id="ticketDisplay"></div>
            <button class="btn" id="checkResultBtn">Check Result</button>
            <div id="resultDisplay"></div>
        </div>
    </section>

    <!-- Profile Section -->
    <section id="profileSection" class="section">
        <div class="container">
            <h2>Your Profile</h2>
            <p><strong>Username:</strong> <span id="profileUsername"></span></p>
            <p><strong>Email:</strong> <span id="profileEmail"></span></p>
            <button class="btn" id="editProfileBtn">Edit Profile</button>
            <div id="editProfileDiv" style="display:none;">
                <input type="email" id="editEmail" placeholder="New Email">
                <input type="password" id="editPassword" placeholder="New Password">
                <button class="btn" id="saveProfileBtn">Save</button>
            </div>
            <p id="profileMessage"></p>
        </div>
    </section>

    <!-- Recharge Section -->
    <section id="rechargeSection" class="section">
        <div class="container">
            <h2>Recharge Your Balance</h2>
            <input type="number" id="rechargeAmount" placeholder="Enter amount to recharge" min="10" required>
            <button class="btn" id="rechargeBalanceBtn">Recharge</button>
            <p id="rechargeMessage"></p>
        </div>
    </section>

    <!-- Ticket History Section -->
    <section id="ticketHistorySection" class="section">
        <div class="container">
            <h2>Ticket History</h2>
            <button class="btn" id="buyTicketBtn">Buy Ticket (₹100)</button>
            <div id="ticketHistory"></div>
        </div>
    </section>

    <!-- Balance Section -->
    <section id="balanceSection" class="section">
        <div class="container">
            <h2>Your Balance: ₹<span id="balanceAmount">0</span></h2>
        </div>
    </section>

    <script src="app.js"></script>
</body>
</html>
