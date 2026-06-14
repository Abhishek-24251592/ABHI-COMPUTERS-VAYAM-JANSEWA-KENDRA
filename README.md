<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DIYA INDIAN GROUP OF INSTITUTIONS</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:linear-gradient(135deg,#007bff,#ffffff);
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;
}

.container{
    width:100%;
    max-width:900px;
    background:#fff;
    padding:30px;
    border-radius:15px;
    box-shadow:0 0 20px rgba(0,0,0,0.15);
}

h1{
    text-align:center;
    color:#0056b3;
    margin-bottom:25px;
}

.form-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
}

.form-group{
    display:flex;
    flex-direction:column;
}

.full-width{
    grid-column:1/3;
}

label{
    margin-bottom:5px;
    font-weight:bold;
    color:#333;
}

input, select, textarea{
    padding:12px;
    border:1px solid #ccc;
    border-radius:8px;
    font-size:14px;
}

input:focus,
select:focus,
textarea:focus{
    outline:none;
    border-color:#007bff;
}

textarea{
    resize:vertical;
}

.btn-group{
    margin-top:20px;
    display:flex;
    gap:10px;
}

button{
    flex:1;
    padding:12px;
    border:none;
    border-radius:8px;
    font-size:16px;
    cursor:pointer;
}

.submit-btn{
    background:#007bff;
    color:white;
}

.reset-btn{
    background:#dc3545;
    color:white;
}

.success{
    display:none;
    text-align:center;
    background:#d4edda;
    color:#155724;
    padding:10px;
    margin-bottom:15px;
    border-radius:8px;
}

@media(max-width:768px){
    .form-grid{
        grid-template-columns:1fr;
    }

    .full-width{
        grid-column:auto;
    }
}
</style>
</head>

<body>

<div class="container">

<h1>DIYAA INDIAN GROUP OF INSTITUTIONS <br>Helpline No.: +91 99848 92174</h1>

<div class="success" id="successMsg">
Form Submitted Successfully!
</div>

<form id="admissionForm">

<div class="form-grid">

<div class="form-group">
<label>Student Name *</label>
<input type="text" name="studentName" required>
</div>

<div class="form-group">
<label>Father's Name *</label>
<input type="text" name="fatherName" required>
</div>

<div class="form-group">
<label>Mother's Name</label>
<input type="text" name="motherName">
</div>

<div class="form-group">
<label>Mobile Number *</label>
<input type="tel" name="mobile" pattern="[0-9]{10}" required>
</div>

<div class="form-group">
<label>Alternate Mobile Number</label>
<input type="tel" name="altMobile" pattern="[0-9]{10}">
</div>

<div class="form-group">
<label>Email Address</label>
<input type="email" name="email">
</div>

<div class="form-group">
<label>Date of Birth</label>
<input type="date" name="dob">
</div>

<div class="form-group">
<label>Gender</label>
<select name="gender">
<option value="">Select Gender</option>
<option>Male</option>
<option>Female</option>
<option>Other</option>
</select>
</div>

<div class="form-group full-width">
<label>Full Address</label>
<textarea name="address" rows="3"></textarea>
</div>

<div class="form-group">
<label>District</label>
<input type="text" name="district">
</div>

<div class="form-group">
<label>State</label>
<input type="text" name="state">
</div>

<div class="form-group">
<label>PIN Code</label>
<input type="text" name="pincode">
</div>

<div class="form-group">
<label>Qualification</label>
<input type="text" name="qualification">
</div>


<div class="form-group">
<label>Course Selection</label>

<select name="course" required>

<optgroup label="Computer Courses">
<option>CCC</option>
<option>DCA</option>
<option>ADCA</option>
<option>PGDCA</option>
<option>O Level</option>
<option>CCA</option>
<option>Tally Prime with GST</option>
<option>Advanced Excel</option>
<option>Data Entry Operator</option>
<option>COPA</option>
<option>Java</option>
</optgroup>

<optgroup label="ITI Trades">
<option>Electrician</option>
<option>Fitter</option>
<option>Welder</option>
<option>COPA</option>
<option>Plumber</option>
<option>Refrigeration & Air Conditioning</option>
</optgroup>

<optgroup label="University Courses">
<option>BA</option>
<option>B.Sc</option>
<option>MA</option>
<option>MBA</option>
<option>Polytechnic</option>
<option>B.Tech</option>
<option>M.Tech</option>
</optgroup>

</select>
</div>

</div>
<div class="form-group">
    <label>Employee ID *</label>
    <input type="text" name="employeeId" placeholder="Enter Employee ID" required>
</div>


<div class="btn-group">
<button type="submit" class="submit-btn">Submit</button>
<button type="reset" class="reset-btn">Reset</button>
</div>

</form>
</div>

<script>
const form = document.getElementById("admissionForm");

form.addEventListener("submit", function(e){
    e.preventDefault();

    const data = new FormData(form);

    let message =
`*New Admission Form*

*Student Name:* ${data.get("studentName")}
*Father Name:* ${data.get("fatherName")}
*Mother Name:* ${data.get("motherName")}
*Employee ID:* ${data.get("employeeId")}
*Mobile:* ${data.get("mobile")}
*Email:* ${data.get("email")}
*Course:* ${data.get("course")}
*Address:* ${data.get("address")}
`;

    let whatsappURL =
    "https://wa.me/919984892174?text=" +
    encodeURIComponent(message);

    window.open(whatsappURL, "_blank");

    document.getElementById("successMsg").style.display = "block";
    form.reset();
});
</script>

</body>
</html>
