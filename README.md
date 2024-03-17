# Hotel Booking Smart Contract

This Solidity smart contract, named HotelBooking, facilitates booking and cancellation of rooms in a hotel. It allows users to book available rooms by sending the required payment in Ether and provides functionality for canceling bookings and withdrawing funds by the owner.

# Features

- `Booking Rooms`: Users can book available rooms by specifying the room number and sending the required payment in Ether.
  Cancellation of Bookings: The contract owner or the contract itself can cancel bookings made by users.

- `Funds Withdrawal`: The contract owner can withdraw the accumulated funds from the contract.
  View Available Rooms: Users can view the list of available rooms at any time.

- `View Contract Balance`: Users can check the current balance of the contract.

# Contract Structure

- `owner`: Address of the contract owner.
- `bookedRooms`: Mapping to track the booking status of rooms for each customer.
- `availableRooms`: Mapping to track the availability status of rooms.
- `numRooms`: Constant representing the total number of rooms available.
- `roomPrice`: Constant representing the price of booking a room. -`RoomBooked event`: Event emitted when a room is successfully booked.
- `Custom errors`: invalidRoom and insufficientFunds are custom errors for handling invalid room numbers and insufficient funds, respectively.
  Functions
- `bookRoom(uint roomNumber, address customer)`: Allows users to book a room by specifying the room number and sending the required payment.
- `cancelBooking(uint roomNumber, address customer)`: Allows the contract owner or the contract itself to cancel bookings made by users.
- `withdrawFunds()`: Allows the contract owner to withdraw accumulated funds from the contract.
- `getAvailableRooms()`: Retrieves the list of currently available rooms.
- `getBalance()`: Retrieves the current balance of the contract.
  Fallback function: Allows the contract to receive Ether.
