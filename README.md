# **Project Overview**

This repository contains performance testing scripts and reports for two scenarios using Apache JMeter:

- Booking API Performance Testing

- Dmoney API Performance Testing

The project includes load testing, stress testing, and dynamic transaction simulations to evaluate system performance under various conditions.

---

## **Prerequisites**

- Install Apache JMeter (version 5.5 or higher recommended).

- Ensure the required environment and network permissions to access the following APIs: Booking API, Dmoney API (API details provided as per project requirements).

- Download or clone this repository: `git clone https://github.com/your-username/Jmeter-Performance-Testing`

---

## **Reports and Screenshots**
### Booking API Load Testing Request Summary and Statistics
![BookingJmeterReport3](https://github.com/user-attachments/assets/f1fd0e4b-f274-4942-ba3a-d2fdf9119fed)

### Booking API Stress Testing Request Summary and Statistics
![BookingJmeterStressReport](https://github.com/user-attachments/assets/118358f0-0be3-41d4-8c76-0e00e8188cad)

### Booking API Jmeter Summary Report (5 minutes load)
![5minutes](https://github.com/user-attachments/assets/79e8a802-cea0-45d9-8c6d-156877facf0d)


### Dmoney API Performance Testing Request Summary and Statistics
![DmoneyJmeterReport1](https://github.com/user-attachments/assets/c525762c-d19f-4d61-88aa-fec721838c17)
![DmoneyJmeterReport2](https://github.com/user-attachments/assets/2371881d-4910-434a-8edf-679db16ea5d9)

---

## How to Run the Tests
### Booking API Test

- Set up JMeter

- Open JMeter

- Load the booking.jmx file

- Run the Test command using cmd for generating report: `jmeter -n -t '.\booking.jmx' -l '.\booking.jtl' -e -o Reports`


### Steps Included in Booking API Test:

- Login API:

- Endpoint: https://restful-booker.herokuapp.com/auth

- Body:
`{
  "username": "admin",
  "password": "password123"
}`

- Create Booking API:

- Endpoint: https://restful-booker.herokuapp.com/booking

- Body:

`{
  "firstname": "Generate Random FirstName",
  "lastname": "Generate Random LastName",
  "totalprice": Generate random amount,
  "depositpaid": true,
  "bookingdates": {
    "checkin": "2024-01-01",
    "checkout": "2024-01-02"
  }
}`

- Search Booking API:

- Endpoint: https://restful-booker.herokuapp.com/booking/<booking_id>

### Load Test:

3 Steps:

- 5-minute load test.

- 10-minute load test.

- 20-minute load test.

#### Gaussian Random Timer: Deviation 2000ms, Constant Delay 500ms.
![Gaussian Time](https://github.com/user-attachments/assets/a3537c8a-a345-4fbe-864e-e55583ca299e)


### Stress Test:

- Gradually increase users to identify bottleneck throughput.

- Breakdown server performance in steps and capture stress points.

---

## Reports

Load Test and Stress Test results are in booking-api-test-report.xlsx under respective tabs (load test report, stress test report).

HTML reports are available in the Reports folder.

---
## Contributor

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/NaimurRahman-11">
        <img src="https://github.com/user-attachments/assets/0388c8e4-b23d-4889-9091-f0299a8823f3" width="200" height="200" alt="Naimur Rahman"/>
        <br />
        <b>Naimur Rahman</b>
      </a>
      <br />
      Software Developer Engineer in Test
      💻 Crafting quality software, one test case at a time.
      📧 nirzon.naim@gmail.com 
    </td>
  </tr>
  <tr>
    <p>📫 <a href="https://github.com/NaimurRahman-11">GitHub Profile</a></p>
      <p>💼 <a href="https://linkedin.com/in/naimurrahman11">LinkedIn Profile</a></p>
  </tr>
</table>

