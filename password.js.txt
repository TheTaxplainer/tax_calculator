(function() {
  // Check if already authenticated
  if (!sessionStorage.getItem('taxplainerAccess')) {
    // Prompt for password
    const password = prompt("Please enter your TAXPLAINED! access code:");
    
    // Replace 'your-secret-code' with whatever password you want to use
    if (password !== 'FileITR0415') {
      alert("Access denied. This calculator is only available to TAXPLAINED! customers.");
      window.location.href = "www.thetaxplainer.com\taxplained"; // Replace with your sales page URL
    } else {
      // Store authentication for this session
      sessionStorage.setItem('taxplainerAccess', 'true');
    }
  }
})();