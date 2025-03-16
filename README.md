# Car Rental Management System

## Overview
The **Car Rental Management System** is a console-based Python application that allows users to manage car rentals efficiently. It enables adding, removing, and renting cars while maintaining a record of rented vehicles. The system uses **SQLite** for database management.

## Features
- **Add New Vehicles**: Store car details such as ID, number, name, seat capacity, luggage capacity, and rental price.
- **Remove Vehicles**: Delete cars from the system.
- **View Available Vehicles**: Display all available cars in the database.
- **Rent a Vehicle**: Users can rent a car by providing their details and rental period.
- **Return a Vehicle**: Update the database when a rented car is returned.
- **Calculate Rent**: The system calculates rental charges based on the number of days the car is rented.
- **UPI Payment Simulation**: The system simulates a UPI payment process for car rentals.

## Technologies Used
- **Python**: Main programming language.
- **SQLite**: Lightweight database to store car and rental records.
- **Datetime**: For managing rental periods.

## Installation
1. **Clone the repository**:
   ```sh
   git clone https://github.com/LalaOp1105/Car-Rental-Management.git
   ```
2. **Navigate to the project directory**:
   ```sh
   cd Car-Rental-Management
   ```
3. **Install dependencies**:
   ```sh
   pip install sqlite3
   ```
4. **Run the program**:
   ```sh
   python car_rental.py
   ```

## Database Schema
### Cars_info Table
| Column Name       | Data Type  | Description |
|-------------------|-----------|-------------|
| Car_id           | INTEGER   | Unique car identifier (Primary Key) |
| Car_no           | TEXT      | Car registration number |
| Car_name         | TEXT      | Car model/name |
| Seats_capacity   | INTEGER   | Number of seats available |
| Luggage_capacity | INTEGER   | Luggage capacity of the car |
| Vehicle_rent     | REAL      | Rent per day |

### Rented_cars Table
| Column Name        | Data Type  | Description |
|--------------------|-----------|-------------|
| User_id           | INTEGER   | Unique user identifier |
| Car_id           | INTEGER   | Foreign key referencing `Cars_info` |
| User_name        | TEXT      | Name of the person renting the car |
| Departure_date   | TEXT      | Start date of rental |
| Arrival_date     | TEXT      | End date of rental |
| Contact_no       | TEXT      | User's contact number |
| Total_amount     | REAL      | Calculated total rental amount |

## Usage Guide
1. **Add a Car**
   - Provide car details (ID, number, name, seats, luggage capacity, rent).
2. **Remove a Car**
   - Enter the car ID to delete it from the database.
3. **View Available Cars**
   - Displays all cars stored in the `Cars_info` table.
4. **Rent a Car**
   - Select a car and enter your details.
   - Enter the departure and arrival dates.
   - The system calculates the rent.
   - Enter UPI ID to simulate payment.
5. **Return a Car**
   - Enter the car ID to mark it as returned.

## Future Enhancements
- Implement a **GUI version** using Tkinter or PyQt.
- Add **real payment gateway integration**.
- Improve **error handling and input validation**.

## License
This project is licensed under the MIT License.



