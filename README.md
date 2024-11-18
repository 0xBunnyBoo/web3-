my-ethereum-website/
├── index.html
├── styles.css
└── script.js



    
    
    
    


    <h1>Connect to Ethereum Wallet</h1>
    Connect Wallet
    <p>Not connected</p>

    
    


body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin-top: 50px;
}

h1 {
    color: #333;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}

p {
    margin-top: 20px;
    font-size: 18px;
    color: #666;
}
document.getElementById('connectButton').addEventListener('click', async () =&gt; {
    if (window.ethereum) {
        try {
            // درخواست دسترسی به حساب‌های کاربری
            const accounts = await window.ethereum.request({ method: 'eth_requestAccounts' });
            // اتصال به حساب کاربری
            document.getElementById('account').textContent = `Connected: ${accounts[0]}`;
        } catch (error) {
            console.error('User denied account access', error);
        }
    } else {
        console.error('No Ethereum provider found. Install MetaMask.');
    }
});
git clone https://github.com/YOUR_USERNAME/my-ethereum-website.git
git add .
git commit -m "Initial commit"
git push origin main
