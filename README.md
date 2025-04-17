# TechnoMinds_hackgenx
Smart &amp; Sustainable E-Waste Management – Scalable solutions for responsible e-waste disposal

My Colab Link of my model which detects image is a e waste or not https://colab.research.google.com/drive/1OIpFVmSvf9jV1WtH67BlKgWR5BbGde_A#scrollTo=d0ekHdGhnrhj
The above colaboratory is in progress and it checks for epochs

My dataset link of image datasets   https://drive.google.com/file/d/17PlBI7Ol0u91buiRqa1am_OV3JWcrBRH/view?usp=drive_link

My prot.io link and its exported .pdf of dummy model is provided below:
https://pr.to/7Y80QL/
[_EcoBot.pdf](https://github.com/user-attachments/files/19777446/_EcoBot.pdf)


Suggestions from Mentor Round 1: We initially use mobilenetv2 pretained model of tensorflow module packages so suggestion from panel is not used pretained models for image classification. So by discussing now we trained our model using cnn by applying its algorithm in our model.
We also do text classification to give suggestion as repair/dispose for that we have made our own dataset I attached it below
[User_Input.csv](https://github.com/user-attachments/files/19777684/User_Input.csv) and below is my colab link that work i had be done till now 
https://colab.research.google.com/drive/1OIpFVmSvf9jV1WtH67BlKgWR5BbGde_A?usp=sharing 
Now our task 2 is doing our model trained according to suggestions.


I have completed my Frontend of Welcome Login/SignUp Page.

\\ Login Page Code
// src/components/LoginPage.js
import React, { useState } from "react";
import { useNavigate } from "react-router-dom"; // Import the hook
import "./LoginPage.css";



const LoginPage = () => {
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");
  const [role, setRole] = useState("");

  const navigate = useNavigate(); // Initialize navigate

  const handleLogin = () => {
    if (!email || !password || !role) {
      alert("Please fill in all fields.");
      return;
    }
  
    // In real app, you'd verify credentials from backend.
    // For now, we simulate successful login:
    alert(`Logging in as ${role} with email: ${email}`);
    navigate("/dashboard"); // 🔁 Redirect to Dashboard after login
  };
  
  return (
    <div className="login-container">
      <h1>Login to EcoBot</h1>

      <input
        type="email"
        placeholder="Email ID"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
        className="login-input"
      />

      <input
        type="password"
        placeholder="Password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
        className="login-input"
      />

      <label className="role-label">Select Your Role</label>
      <select
        value={role}
        onChange={(e) => setRole(e.target.value)}
        className="login-select"
      >
        <option value="">-- Choose Role --</option>
        <option value="User">User</option>
        <option value="Shopkeeper">Shopkeeper</option>
        <option value="Recycle Hub">Recycle Hub</option>
      </select>

      <div className="login-button-container">
        <button className="btn back-btn" onClick={() => navigate("/")}>
          ← Back
        </button>
        <button className="btn login-btn" onClick={handleLogin}>
          Login →
        </button>
      </div>
    </div>
  );
};

export default LoginPage;

// And below is LoginPages.css
/* Main page background */
body {
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #e0f7e9, #c8e6c9); /* soft green gradient */
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  /* Main login card */
  .login-container {
    max-width: 400px;
    width: 90%;
    padding: 30px;
    background-color: #ffffff;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
  }
  
  /* Input fields styling */
  .login-input,
  .login-select {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border-radius: 8px;
    border: 1px solid #ccc;
    font-size: 1rem;
  }
  
  /* Label styling */
  .role-label {
    font-weight: bold;
    margin-top: 15px;
    display: block;
    text-align: left;
    color: #2e7d32;
  }
  
  /* Button container */
  .login-button-container {
    display: flex;
    justify-content: space-between;
    margin-top: 25px;
  }
  
  /* General button styling */
  .btn {
    padding: 12px 20px;
    font-size: 1rem;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-weight: 600;
    width: 48%;
    border: none;
  }
  
  /* Back button */
  .back-btn {
    background-color: #a5d6f9;
    color: #0d47a1;
  }
  
  .back-btn:hover {
    background-color: #64b5f6;
  }
  
  /* Login button */
  .login-btn {
    background-color: #43a047;
    color: white;
  }
  
  .login-btn:hover {
    background-color: #2e7d32;
  }


  Recycle-Hub Frontend:
![WhatsApp Image 2025-04-14 at 01 37 40_71dd84ef](https://github.com/user-attachments/assets/27e2a3fa-5bf2-444a-89bd-b05b1ea2e9de)
![WhatsApp Image 2025-04-14 at 01 47 43_a556fab9](https://github.com/user-attachments/assets/0037e5cc-6f39-4d61-8c6a-09e95f5039d0)

 Shopkeeper Dashboard:

![WhatsApp Image 2025-04-14 at 00 47 28_489aeb48](https://github.com/user-attachments/assets/6f277d26-9c63-4c62-b63d-7c3f08986f80)
![WhatsApp Image 2025-04-14 at 01 14 01_a64ca0e2](https://github.com/user-attachments/assets/eff5c559-ad89-44be-9ce6-9fe82420ac19)
![WhatsApp Image 2025-04-13 at 19 54 54_b1aca719](https://github.com/user-attachments/assets/d7ad834f-7a50-46db-83ae-f3ada1899881)

Admin Dashboard :

![WhatsApp Image 2025-04-17 at 12 17 08_73015ff6](https://github.com/user-attachments/assets/6ee38aa3-accc-450a-b0c3-bb64f2ae12c6)

![WhatsApp Image 2025-04-17 at 12 16 38_47b8e9f8](https://github.com/user-attachments/assets/3cfe1eac-31c7-494a-8caa-606b14dcd2e4)

![WhatsApp Image 2025-04-17 at 12 17 43_f6a3b14a](https://github.com/user-attachments/assets/d08198ed-b78d-44eb-a62e-406caf39dd30)









