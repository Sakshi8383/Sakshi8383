- 👋 Hi, I’m @Sakshi8383
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Sakshi8383/Sakshi8383 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Expense Tracker</title>
    <!-- Add Bootstrap CSS link -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
          integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8sh+WyIx8/ow+rnjEep98z1RSQQVdP5uMI21EkN"
          crossorigin="anonymous">
</head>
<body class="container mt-5">
    <h1 class="mb-4">Expense Tracker</h1>
    <form action="{{ url_for('add_expense') }}" method="post">
        <div class="form-group">
            <label for="description">Description:</label>
            <input type="text" class="form-control" name="description" required>
        </div>
        <div class="form-group">
            <label for="amount">Amount:</label>
            <input type="number" class="form-control" name="amount" required>
        </div>
        <button type="submit" class="btn btn-primary">Add Expense</button>
    </form>
    <h2 class="mt-4">Expenses:</h2>
    <ul class="list-group">
        {% for expense in expenses %}
            <li class="list-group-item">{{ expense.description }} - ${{ expense.amount }}</li>
        {% endfor %}
    </ul>

    <!-- Add Bootstrap JS and Popper.js (for Bootstrap's JavaScript components) -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"
            integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj"
            crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js"
            integrity="sha384-gtQ8r/JATAdFZ04mtfB6Llgu6niMzXsUDxnyHyJUCAjFqZz5C+5bx2TA2F5FbbhG"
            crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"
            integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8sh+WyIx8/ow+rnjEep98z1RSQQVdP5uMI21EkN"
            crossorigin="anonymous"></script>
</body>
</html>
