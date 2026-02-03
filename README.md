<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Family Tree - All Visible</title>
    <style>
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background-color: #f8f9fa;
            text-align: center;
            padding: 20px;
        }

        h1 { color: #2c3e50; }

        /* The Tree Container */
        .tree ul {
            padding-top: 20px; 
            position: relative;
            display: flex;
            justify-content: center;
            list-style-type: none;
            padding-left: 0;
        }

        .tree li {
            float: left; text-align: center;
            list-style-type: none;
            position: relative;
            padding: 20px 10px 0 10px;
        }

        /* Connecting Lines (Horizontal) */
        .tree li::before, .tree li::after {
            content: '';
            position: absolute; top: 0; right: 50%;
            border-top: 2px solid #adb5bd;
            width: 50%; height: 20px;
        }
        .tree li::after {
            right: auto; left: 50%;
            border-left: 2px solid #adb5bd;
        }

        /* Remove lines for single children or edges */
        .tree li:only-child::after, .tree li:only-child::before { display: none; }
        .tree li:only-child { padding-top: 0; }
        .tree li:first-child::before, .tree li:last-child::after { border: 0 none; }
        .tree li:last-child::before { border-right: 2px solid #adb5bd; border-radius: 0 5px 0 0; }
        .tree li:first-child::after { border-radius: 5px 0 0 0; }

        /* Vertical Connector to Parents */
        .tree ul ul::before {
            content: '';
            position: absolute; top: 0; left: 50%;
            border-left: 2px solid #adb5bd;
            width: 0; height: 20px;
        }

        /* The Person Card/Tile */
        .person {
            background: white;
            border: 2px solid #457b9d;
            border-radius: 8px;
            padding: 15px;
            display: inline-block;
            min-width: 140px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .person img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #e9ecef;
            margin-bottom: 10px;
        }

        .person span {
            display: block;
            font-weight: bold;
            color: #1d3557;
        }

        .person small {
            display: block;
            color: #6c757d;
            font-size: 0.8em;
            margin-top: 5px;
        }
    </style>
</head>
<body>

    <h1>Our Family Tree</h1>

    <div class="tree">
        <ul>
            <li>
                <div class="person">
                    <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Grandpa">
                    <span>Grandfather</span>
                    <small>1945 - 2010</small>
                </div>
                
                <ul>
                    <li>
                        <div class="person">
                            <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Father">
                            <span>Father</span>
                            <small>Engineer</small>
                        </div>
                        <ul>
                            <li>
                                <div class="person">
                                    <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Me">
                                    <span>Me (Student)</span>
                                </div>
                            </li>
                            <li>
                                <div class="person">
                                    <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Sister">
                                    <span>Sister</span>
                                </div>
                            </li>
                        </ul>
                    </li>

                    <li>
                        <div class="person">
                            <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Uncle">
                            <span>Uncle</span>
                            <small>Chef</small>
                        </div>
                        <ul>
                            <li>
                                <div class="person">
                                    <img src="C:\Users\ankit\OneDrive\Desktop\person.png" alt="Cousin">
                                    <span>Cousin </span>
                                </div>
                            </li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </div>

</body>
</html> 
