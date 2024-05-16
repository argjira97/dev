Certainly! Let's create a simple HTML code for an event countdown. This code will count down to a specific date and time, and it will update dynamically:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event Countdown</title>
    <style>
        .countdown {
            font-family: Arial, sans-serif;
            text-align: center;
            font-size: 24px;
        }
    </style>
</head>
<body>

<div class="countdown" id="countdown"></div>

<script>
    // Set the date we're counting down to
    var countDownDate = new Date("May 31, 2024 00:00:00").getTime();

    // Update the countdown every 1 second
    var x = setInterval(function() {

        // Get the current date and time
        var now = new Date().getTime();

        // Calculate the remaining time
        var distance = countDownDate - now;

        // Calculate days, hours, minutes, and seconds
        var days = Math.floor(distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        var seconds = Math.floor((distance % (1000 * 60)) / 1000);

        // Display the countdown
        document.getElementById("countdown").innerHTML = days + "d " + hours + "h "
            + minutes + "m " + seconds + "s ";

        // If the countdown is finished, display a message
        if (distance < 0) {
            clearInterval(x);
            document.getElementById("countdown").innerHTML = "The event has already happened!";
        }
    }, 1000);
</script>

</body>
</html>
```

This code creates a countdown timer that counts down to May 31, 2024, at midnight. You can adjust the `countDownDate` variable to the date and time of your event. The countdown will update every second until the specified date and time are reached.