<!DOCTYPE html>
<html>
<head>
  <title>Aadhaar Application Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      padding: 20px;
    }
    .form-container, .success-container {
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 {
      text-align: center;
      color: #333;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }
    input, select {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
    button {
      margin-top: 20px;
      padding: 10px;
      width: 100%;
      background-color: #28a745;
      color: white;
      border: none;
      border-radius: 4px;
      font-size: 16px;
    }
    .success-message {
      text-align: center;
      color: green;
      font-size: 20px;
    }
  </style>
</head>
<body>

  <div class="form-container" id="formDiv">
    <h2>Aadhaar Application Form</h2>
    <form id="aadhaarForm">
      <label for="name">Full Name</label>
      <input type="text" id="name" required>

      <label for="dob">Date of Birth</label>
      <input type="date" id="dob" required>

      <label for="gender">Gender</label>
      <select id="gender" required>
        <option value="">--Select--</option>
        <option>Male</option>
        <option>Female</option>
        <option>Other</option>
      </select>

      <label for="address">Address</label>
      <input type="text" id="address" required>

      <label for="mobile">Mobile Number</label>
      <input type="tel" id="mobile" pattern="[0-9]{10}" required>

      <label for="email">Email</label>
      <input type="email" id="email" required>

      <button type="submit">Submit</button>
    </form>
  </div>

  <div class="success-container" id="successDiv" style="display: none;">
    <h2>Application Status</h2>
    <p class="success-message">🎉 Aadhaar Application Submitted Successfully!</p>
  </div>

  <script>
    document.getElementById("aadhaarForm").addEventListener("submit", function(e) {
      e.preventDefault(); // Prevent form from actually submitting
      document.getElementById("formDiv").style.display = "none";
      document.getElementById("successDiv").style.display = "block";
    });
  </script>

</body>
</html>
