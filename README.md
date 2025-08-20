

Project Overview <br>
Dream Nest is an all-in-one online platform that simplifies buying, renting, and decorating homes. It caters to diverse user roles such as renters, buyers, builders, home decorators, and administrators. Dream Nest focuses on streamlining real estate transactions and property management through a user-friendly interface.

Motivation
Real estate tasks, including property management, sales, rentals, and renovations, are often complex and time-intensive. Dream Nest addresses these challenges by offering a unified platform where users can handle all their real estate needs with ease. Whether selling a home, exploring rental options, or managing relocation and renovation services, Dream Nest ensures speed, convenience, and efficiency.

Feature List
Dream Nest offers a robust set of functionalities:
1.	User Management:
o	Registration and login.
o	Role-based access (e.g., user, builder, admin).
2.	Property Listings:
o	Adding properties for sale or rent.
o	Including details like price, type, status, and images.
3.	Rental Reviews:
o	Allowing users to submit and view reviews of rental services.
4.	Service Management:
o	Tracking relocation, packing, and renovation services.
5.	Transactions:
o	Logging transaction details (amount, reference, status).
6.	Balance Tracking:
o	Maintaining and updating user financial records.
7.	Search and Filter Options:
o	Enabling property and service searches with specific filters.
8.	Notifications:
o	Informing users of updates on bookings, transactions, and services.
9.	Administrative Dashboard:
o	Monitoring platform activity and managing user roles and permissions.



Database Design Approach
The database for Dream Nest is structured to ensure efficient data management and retrieval while maintaining clear relationships between entities.

Key Tables and Attributes
1.	User Table: Stores user details and roles.
o	Attributes: id, name, email, password, access_token, role.
2.	House List Table: Contains property details for sale or rent.
o	Attributes: serial_number, author, currently_owned_by, image_link, description, price, address, details, type, status.
3.	Rent Review Table: Logs user feedback on rental services.
o	Attributes: serial_number, client, comment.
4.	Services Table: Tracks service requests like moving and renovation.
o	Attributes: serial_number, service, cost, done_by, status.
5.	Transaction Table: Records financial transactions.
o	Attributes: author, transaction_id, amount, reference, status.
6.	User Balance Table: Maintains user financial balances.
o	Attributes: author, balance.

Relationships Between Entities
•	User to House List: One builder can list multiple properties.
o	Foreign Key: author in House List references id in User Table.
•	User to Rent Review: One user can leave multiple reviews.
o	Foreign Key: client in Rent Review references id in User Table.
•	User to Services: One user can request multiple services.
o	Foreign Key: done_by in Services references id in User Table.
•	User to Transactions: One user can initiate multiple transactions.
o	Foreign Key: author in Transaction references id in User Table.
•	User to Balance: One user has one balance record.
o	Foreign Key: author in User Balance references id in User Table.
o	
Data Integrity and Optimization
•	Normalization: Minimizes redundancy and ensures data consistency.
•	Indexes: Key fields (e.g., id, transaction_id, email) are indexes for faster queries.
•	Constraints: Foreign keys and unique constraints maintain data integrity.
Scalability and Extendibility
•	Modular table design supports easy addition of new features and roles.


•	Relationships ensure flexibility for incorporating advanced analytics or future enhancements.


Technology Stack
1.	Database Management: MySQL for efficient data handling.
2.	Front-End & Back-End:
o	HTML: Structure.
o	CSS: Styling.
o	JavaScript: Interactivity.
o	PHP: Server-side logic.
o	MySQL: Database management

Limitations:
• No 3D models or virtual tours for property visualization.
• Limited search filters (e.g., room count, floor number, property size).
• No support for bank or mobile payments.
• No personalized property recommendations.
• No rent payment tracking module.

Future works:
•   Simplify Searching
•	More sorting options: Sort by price, rooms, floor, size, or proximity to schools and shops.
•	Advanced filters: Filter by pool, gym, parking, pet-friendly, elevator, security, balcony size, and neighborhood.
•	Keyword search: Find flats using terms like "balcony" or "near the park."
•   Enhance Experience
•	3D tours: View flats in 3D or take virtual tours.


•   Simplify Payments
•	Direct bank payments: Pay directly from your bank account.
•	Mobile payments: Use Google Pay, Apple Pay, etc.
•	Installments: Pay in smaller parts over time.
•   Personalized Assistance
•	Flat suggestions: Get recommendations based on preferences.
•	User profiles: Save preferences and budget for better matches.
•	Notifications: Alerts for new matching flats.
•   Better Rent Management
•	Track payments: Keep track of rent, get reminders, and pay easily.
•   Stronger Security
•	Hacker protection: Enhance system security.
•	Data safety: Safeguard personal information.
•   Extra Features
•	Landlord tools: Help landlords manage flats and communicate with tenants.
•	Chat options: Directly chat with landlords.
•	
Conclusion:
This project aims to help people find and rent properties. We created an ER diagram to plan the system, focusing on key elements like houses, users, and payments. Currently, the system lets users list houses and create accounts. Future improvements include better search options, adding house photos and 3D models, and simplifying payments. These updates will make the platform more helpful for renters and property owners.
