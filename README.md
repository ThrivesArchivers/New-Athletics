<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>New Athletics Treasury Office</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family: Arial, sans-serif;
    }

    body{
        background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
        color:white;
        padding:30px;
    }

    .container{
        max-width:900px;
        margin:auto;
        background: rgba(255,255,255,0.08);
        padding:30px;
        border-radius:20px;
        box-shadow:0 0 20px rgba(0,0,0,0.5);
    }

    h1{
        text-align:center;
        margin-bottom:20px;
        color:#00ffcc;
        font-size:40px;
    }

    h2{
        margin-top:25px;
        color:#ffd700;
        border-bottom:2px solid #fff;
        padding-bottom:8px;
    }

    .member-list{
        margin-top:15px;
    }

    .member{
        display:flex;
        justify-content:space-between;
        background:rgba(255,255,255,0.1);
        padding:12px;
        margin-bottom:10px;
        border-radius:10px;
    }

    .summary{
        margin-top:20px;
        padding:20px;
        background:rgba(0,0,0,0.3);
        border-radius:15px;
    }

    .summary p{
        margin:10px 0;
        font-size:18px;
    }

    .highlight{
        color:#00ff99;
        font-weight:bold;
    }

    .danger{
        color:#ff4d4d;
        font-weight:bold;
    }

    .note{
        margin-top:25px;
        padding:15px;
        background:#ff9800;
        color:black;
        border-radius:10px;
        font-weight:bold;
        text-align:center;
    }

    button{
        margin-top:20px;
        width:100%;
        padding:15px;
        border:none;
        border-radius:10px;
        background:#00cc99;
        color:white;
        font-size:18px;
        cursor:pointer;
        transition:0.3s;
    }

    button:hover{
        background:#009977;
    }
</style>
</head>

<body>

<div class="container">

    <h1>🏃 New Athletics Treasury Office 💰</h1>

    <h2>Money Received</h2>

    <div class="member-list" id="members"></div>

    <div class="summary">
        <p>💵 Current Balance in Account:
            <span class="highlight">K287</span>
        </p>

        <p>🎁 Donation From System:
            <span class="highlight">K400</span>
        </p>

        <p>⚠️ Donation from Coach:
            <span class="danger">Not Yet Received</span>
        </p>

        <p>🏦 Total Athletics Money:
            <span class="highlight">K687</span>
        </p>
    </div>

    <h2>Expenses</h2>

    <div class="summary">
        <p>📋 Processing of Jessy:
            <span class="danger">K1300</span>
        </p>

        <p>🩹 First Aid / Money Keeping:
            <span class="danger">K200</span>
        </p>

        <p>📌 Total Needed:
            <span class="highlight">K1500</span>
        </p>

        <p>📉 Remaining Needed:
            <span class="danger" id="remaining"></span>
        </p>
    </div>

    <div class="note">
        📢 Starting next season, every member should contribute K50!
    </div>

    <button onclick="showMessage()">
        View Treasury Message
    </button>

</div>

<script>

const members = [
    {name:"Mennah", amount:37},
    {name:"Paul (Captain)", amount:50},
    {name:"The General", amount:50},
    {name:"Nicolas (Vice Captain)", amount:50},
    {name:"Fred", amount:50},
    {name:"Jeff", amount:50}
];

const memberContainer = document.getElementById("members");

members.forEach(member => {
    memberContainer.innerHTML += `
        <div class="member">
            <span>${member.name}</span>
            <span>K${member.amount}</span>
        </div>
    `;
});

const totalNeeded = 1500;
const currentMoney = 687;

const remaining = totalNeeded - currentMoney;

document.getElementById("remaining").innerHTML = "K" + remaining;

function showMessage(){
    alert("🏃 Athletics Treasury Update:Current Available Money: K687 Total Needed: K1500 Remaining Balance Needed: K813 Thank you for supporting Athletics!");
}

</script>

</body>
</html>
