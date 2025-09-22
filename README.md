# airbnb-clone-project


## Team Roles

In order to successfully build and maintain the AirBnB Clone project, the project team will include the following roles:

- **Backend Developer**  
  Responsible for implementing the server-side logic, creating APIs, handling authentication, and ensuring that the application’s backend functions correctly with the database and front-end.

- **Front-End Developer**  
  Responsible for designing and implementing the user interface, ensuring a responsive and intuitive experience, integrating APIs from the backend, and handling client-side functionality.

- **Database Administrator (DBA)**  
  Manages the database, including designing schemas, optimizing queries, ensuring data integrity, and handling backups and migrations.

- **DevOps / Deployment Engineer**  
  Responsible for deployment, server configuration, continuous integration/continuous deployment (CI/CD), and monitoring the application in production.

- **Project Manager**  
  Oversees the project timeline, coordinates team members, manages tasks, and ensures that milestones are met.

- **QA / Tester**  
  Tests the application for bugs, performance issues, and ensures that features meet the project requirements and quality standards.

## Technology Stack

The AirBnB Clone project leverages a variety of technologies to build a full-featured, responsive, and scalable application:

- **Django**: A high-level Python web framework used for building the backend, handling business logic, user authentication, and creating RESTful APIs with Django REST Framework.  

- **Django REST Framework (DRF)**: A toolkit for building Web APIs on top of Django, providing serialization, authentication, and easy handling of HTTP requests.  

- **React**: A JavaScript library used for building the front-end user interface, creating dynamic and responsive web pages, and interacting with the backend APIs.  

- **PostgreSQL**: A relational database management system used to store and manage the project’s data, including user accounts, property listings, bookings, and reviews.  

- **HTML/CSS/JavaScript**: Core front-end technologies used to structure, style, and add interactivity to web pages.  

- **Git & GitHub**: Version control system and repository hosting service used to manage the project’s source code, track changes, and collaborate with team members.  

- **Heroku / AWS (optional)**: Cloud platforms used to deploy the application and make it accessible to users online.


## Database Design

The AirBnB Clone project will include the following key entities:

- **Users**  
  Fields: `id`, `username`, `email`, `password`, `is_host`  
  - Each user can act as a guest or a host.  
  - A user can have multiple properties (if they are a host) and multiple bookings (as a guest).  

- **Properties**  
  Fields: `id`, `title`, `description`, `location`, `price_per_night`, `host_id`  
  - Each property is owned by a host (user).  
  - A property can have multiple bookings and multiple reviews.  

- **Bookings**  
  Fields: `id`, `property_id`, `guest_id`, `start_date`, `end_date`, `total_price`  
  - A booking belongs to a single property and a single guest (user).  

- **Reviews**  
  Fields: `id`, `property_id`, `guest_id`, `rating`, `comment`, `created_at`  
  - Reviews are associated with a property and the guest who left the review.  

- **Payments**  
  Fields: `id`, `booking_id`, `amount`, `payment_method`, `status`, `payment_date`  
  - Each payment is linked to a booking and records the transaction details.  

### Relationships
- A **User** can have multiple **Properties** (as a host).  
- A **User** can have multiple **Bookings** (as a guest).  
- A **Property** can have multiple **Bookings** and **Reviews**.  
- Each **Booking** is linked to one **Property** and one **Guest (User)**.  
- Each **Payment** is associated with a single **Booking**.

