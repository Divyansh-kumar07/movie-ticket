# movie-ticket


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movie Ticket Booking</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>Movie Ticket Booking</h1>
        
        <label for="movie">Select Movie:</label>
        <select id="movie">
            <option value="10">Avengers - $10</option>
            <option value="12">Joker - $12</option>
            <option value="8">Frozen - $8</option>
            <option value="15">Inception - $15</option>
        </select>

        <div class="seat-container">
            <div class="screen"></div>
            <div class="seats">
                <!-- Generating seats dynamically using JavaScript -->
            </div>
        </div>

        <p class="info">Selected Seats: <span id="count">0</span> | Total Price: $<span id="total">0</span></p>
        <button id="book-btn">Book Tickets</button>
    </div>

    <script src="script.js"></script>
</body>
</html>




body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    text-align: center;
    padding: 20px;
}

.container {
    width: 400px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px gray;
}

h1 {
    margin-bottom: 20px;
}

label {
    font-weight: bold;
}

.seat-container {
    margin: 20px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.screen {
    width: 80%;
    height: 50px;
    background: #333;
    margin-bottom: 10px;
    border-radius: 5px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
}

.seats {
    display: grid;
    grid-template-columns: repeat(6, 30px);
    gap: 10px;
}

.seat {
    width: 30px;
    height: 30px;
    background: #ccc;
    border-radius: 5px;
    cursor: pointer;
}

.seat.selected {
    background: green;
}

.seat.occupied {
    background: red;
    cursor: not-allowed;
}

.info {
    font-size: 18px;
}

button {
    background: blue;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background: darkblue;
}
