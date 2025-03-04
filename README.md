<p align="center">
  <a href="https://www.hs-heilbronn.de/de/induko" target="blank"><img src="induko_image.png" width="600" alt="Induko Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

<p align="center">


Heilbronn University is researching advanced technical tools and didactic approaches designed to foster collaboration and interaction. The primary goal is to enhance and facilitate interdisciplinary, inter-faculty, and inter-university cooperation. Through the InduKo research project, we aim to strengthen this collaboration using innovative digital tools and modern, digitally supported strategies that boost motivation and foster innovation through partnership.

Unisync streamlines communication by automating the creation of messenger chat groups that correspond to course rooms in ILIAS. Designed as a lightweight and adaptable solution, Unisync could be adapted and integrated with other learning management systems (LMS) beyond ILIAS. One fundamental constraint in its development was the lack of direct system access to ILIAS. As a result, a web scraper was used to extract course data and transfer it to the Matrix system. This method allows Unisync to function without requiring any modifications to ILIAS or other LMS platforms, preserving their security and system integrity. Additionally, it ensures that the solution remains highly adaptable to different university environments without increasing maintenance complexity or security risks.

Unisync does not require additional software installation for the users - teachers can generate chat groups simply by accessing a link stored in ILIAS or bookmarked in their browser. After logging into the LMS, course data is transferred to the Matrix system, where chat groups are automatically created, participants are assigned, and invitations are sent. These groups can then be accessed through Matrix-based messengers such as Element or FluffyChat. The system’s flexibility, security, and low maintenance requirements make it an efficient and scalable solution for universities looking to enhance digital collaboration. Further information can be found in the PDF document linked above. Unisync showcases how a lightweight solution can create Matrix-based course rooms from LMS data without deep system integration.

Unisync was developed as part of a subproject within the <a href="https://www.hs-heilbronn.de/en/projekt-induko-2cab68e84c21b797" target="_blank">InduKo project (Innovation through Collaboration) </a> , which was funded by <a href="https://stiftung-hochschullehre.de/en/" target="_blank">Stiftung Innovation in der Hochschullehre </a> (August 2021 - July 2024).

</p>

# hnunisync.de - Synchronizing ILIAS Courses with Matrix Rooms

**HNUnisync.de** is a web application designed to streamline communication and collaboration for educational institutions by synchronizing **ILIAS** (a popular learning management system) courses with **Matrix** communication rooms. The tool automates the process of syncing enrolled students from ILIAS into Matrix rooms, creating a seamless integration between course content and collaborative discussion environments.

## Key Features

1. **User Authentication**:
   - Secure login using **HHN (Heilbronn University)** account credentials.
   - Authentication is managed via **OpenID Connect**.
   - Supports **two-step verification** using an authenticator app for added security.

2. **Course Synchronization**:
   - Automatically retrieves course data and enrolled student information from the **ILIAS** platform using web scraping.
   - Displays course and participant information, enabling quick synchronization with Matrix rooms.

3. **Matrix Integration**:
   - Users log into the Matrix server hosted at **[unifyhn.de](https://unifyhn.de)** to complete the course synchronization process.
   - Automatically creates Matrix rooms named after each course and adds enrolled students as members.

4. **Matrix-Based Communication**:
   - Students and instructors can use any Matrix-based messaging app (e.g., **Element** or **FluffyChat**) to join the created rooms and engage in discussions.

## Technologies Used

- **Python FastAPI**: For building the web application.
- **Playwright**: For web scraping ILIAS data.
- **Uvicorn**, **Pydantic**, **Jinja2**, **Gunicorn**: For server deployment, data validation, and template rendering.
- **BeautifulSoup4**: For parsing HTML data from ILIAS.
- **Matrix-Nio**: For interacting with the Matrix protocol.
- **Quart**, **Requests**, **Httpx**: For asynchronous operations and API requests.

## Installation & Setup

1. **Create Virtual Environment**:
   ```bash
   cd hnunisync
   python3 -m venv venv
   source venv/bin/activate
   ```

2. **Create Virtual Environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   
4. **Start the Application**:
   ```bash
   uvicorn main:app --reload
   ```

5. **Access the Web Interface**:
   Open your browser and navigate to **[hnunisync.de](https://hnunisync.de)** to access the HNUnisync interface.

## Usage

- **Login**: Use your **HHN** credentials to log in securely.
- **Synchronize Courses**: Select the courses you want to synchronize and initiate the sync process.
- **Matrix Room Management**: Automatically manages the creation and updating of Matrix rooms for each course.
- **Real-time Collaboration**: Students can join the Matrix rooms using their preferred Matrix-based messaging apps.

## Contributing

Contributions are welcome! If you want to improve this project, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## Contact

For questions or support, please reach out to the repository owner or open an issue in the repository.

## Links

- Project URL: [https://hnunisync.de](https://hnunisync.de)

## Contributing

Contributions are welcome! To contribute to the project, please follow these steps:

1. **Fork the repository**.
2. **Create a new branch** for your feature or bugfix (`git checkout -b feature-name`).
3. **Make your changes** and **commit them** (`git commit -m 'Add a new feature'`).
4. **Push the branch** to your fork (`git push origin feature-name`).
5. **Submit a pull request** to the `main` branch of the original repository.

## Contact

For support or inquiries, please open an issue on the GitHub repository or reach out to the repository owner.

## Links

- Matrix Server URL: [https://unifyhn.de](https://unifyhn.de)

## License
- This project is licensed under [Apache 2.0](LICENSE). Copyright 2024 , Hochschule Heilbronn.

## Acknowledgments

This project was developed as part of the **InduKo Project**, funded by **Stiftung Innovation in der Hochschullehre**. We also acknowledge the support from students, faculty, and contributors who have been part of this collaborative effort.

For more information about the InduKo research project, visit the official website.
