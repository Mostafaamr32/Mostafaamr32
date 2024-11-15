<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حاسب الوقت منذ هدف قفشة</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        h1 {
            font-size: 24px;
        }
        .time {
            font-size: 36px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>الوقت منذ هدف قفشة في نهائي دوري أبطال أفريقيا</h1>
    <div class="time" id="time"></div>

    <script>
        // تاريخ هدف قفشة في نهائي دوري أبطال أفريقيا 2020
        var goalTime = new Date("Nov 27, 2020 21:00:00 GMT+0200");

        function updateTime() {
            var currentTime = new Date();
            var timeDifference = currentTime - goalTime; // فرق الوقت بين اللحظتين

            // حساب الأيام والساعات والدقائق والثواني
            var days = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
            var hours = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((timeDifference % (1000 * 60)) / 1000);

            // عرض الوقت بشكل ديناميكي
            document.getElementById("time").innerHTML = days + " يوم " + hours + " ساعة " + minutes + " دقيقة " + seconds + " ثانية ";
        }

        // تحديث الوقت كل ثانية
        setInterval(updateTime, 1000);
    </script>
</body>
</html>
