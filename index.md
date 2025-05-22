<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Survey</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #555;
        }
        input[type="text"],
        input[type="email"],
        input[type="number"],
        select,
        textarea {
            width: calc(100% - 20px);
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        input[type="radio"],
        input[type="checkbox"] {
            margin-right: 10px;
        }
        .form-group {
            margin-bottom: 25px;
        }
        .radio-group label, .checkbox-group label {
            font-weight: normal; /* Override bold for individual radio/checkbox labels */
            display: inline-block;
            margin-bottom: 0;
            margin-right: 15px;
        }
        button {
            display: block;
            width: 100%;
            padding: 12px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
    <script>
        function onSurveySubmit() {
            
            console.log( 'Start::: Survey Submit' );
            console.log( 'End::: Survey Submit' );
            
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>Customer Feedback Survey</h1>
        <form>
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" value="Magulan Duraipandian" required>
            </div>

            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" value="magulan@infallibletechie.com" required>
            </div>

            <div class="form-group">
                <label for="age">Age:</label>
                <input type="number" id="age" name="age" min="18" max="100" value="25">
            </div>

            <div class="form-group">
                <label>How would you rate our product/service?</label>
                <div class="radio-group">
                    <input type="radio" id="rating_excellent" name="rating" value="excellent" required checked>
                    <label for="rating_excellent">Excellent</label>
                    <input type="radio" id="rating_good" name="rating" value="good">
                    <label for="rating_good">Good</label>
                    <input type="radio" id="rating_average" name="rating" value="average">
                    <label for="rating_average">Average</label>
                    <input type="radio" id="rating_poor" name="rating" value="poor">
                    <label for="rating_poor">Poor</label>
                </div>
            </div>

            <div class="form-group">
                <label for="favorite_feature">What is your favorite feature?</label>
                <select id="favorite_feature" name="favorite_feature" value="price">
                    <option value="">-- Please select --</option>
                    <option value="ease_of_use">Ease of Use</option>
                    <option value="customer_support">Customer Support</option>
                    <option value="price">Price</option>
                    <option value="design">Design</option>
                    <option value="other">Other</option>
                </select>
            </div>

            <div class="form-group">
                <label>Which of the following improvements would you like to see? (Select all that apply)</label>
                <div class="checkbox-group">
                    <input type="checkbox" id="improve_features" name="improvements[]" value="more_features" checked>
                    <label for="improve_features">More features</label><br>
                    <input type="checkbox" id="improve_performance" name="improvements[]" value="better_performance">
                    <label for="improve_performance">Better performance</label><br>
                    <input type="checkbox" id="improve_ui" name="improvements[]" value="improved_ui">
                    <label for="improve_ui">Improved user interface</label><br>
                    <input type="checkbox" id="improve_support" name="improvements[]" value="faster_support">
                    <label for="improve_support">Faster customer support</label>
                </div>
            </div>

            <div class="form-group">
                <label for="comments">Any additional comments or suggestions?</label>
                <textarea id="comments" name="comments" rows="5" placeholder="Your comments here..."></textarea>
            </div>

            <button onclick="onSurveySubmit()">Submit Survey</button>
        </form>
    </div>
</body>
</html>
