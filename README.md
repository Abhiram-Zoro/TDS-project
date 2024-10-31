->This script uses the GitHub API to retrieve user data for individuals located in London with over 500 followers.
->The most interesting finding was that most popular London-based GitHub users are actively involved in open-source contributions and have a large number of repositories.
->Developers looking to grow their following could focus on consistent contributions, particularly in open-source projects.

Project Overview:
1)This project scrapes GitHub user data for individuals located in London with over 500 followers by using the GitHub API.
2)One surprising insight was the strong trend among London-based users: they frequently contribute to popular open-source projects, often with more repositories than expected for their followers.
3)Based on the analysis, developers aiming to grow their GitHub presence should consider consistently contributing to open-source repositories, which attracts visibility and followers.


Table of Contents:
1)About the Project
2)Data Collected
3)Installation and Setup
4)Usage Instructions
5)Rate Limiting
6)File Descriptions
7)Limitations and Recommendations

About the Project
This project uses the GitHub API to fetch profiles of users in London with over 500 followers. The data collected includes essential user information and repository details. It is saved in CSV format for easy data analysis, allowing insights into the profiles and projects of popular users.


users.csv - Contains user details, including:

login: GitHub username
name: Full name
company: Cleaned company names (trimmed whitespace, no leading "@", and converted to uppercase)
location: User location
email: Email address (if available)
hireable: Whether the user is open to job opportunities
bio: User bio or description
public_repos: Number of public repositories
followers: Number of followers
following: Number of users they follow
created_at: GitHub account creation date


repositories.csv - Lists each user's public repositories (up to 500 per user), including:

login: GitHub username
full_name: Repository name
created_at: Repository creation date
stargazers_count: Number of stars
watchers_count: Number of watchers
language: Primary language used
has_projects: If projects are enabled
has_wiki: If the repository has a wiki
license_name: License under which the repository is published

Installation and Setup:
1) Clone the Repository
2)Install Required Packages
3)Setup GitHub API Token

Usage Instructions:
1) Run the Script
2) Generated Files

Rate Limiting
GitHub API has rate limits:

Unauthenticated requests: 60 requests per hour.
Authenticated requests: 5,000 requests per hour.

File Descriptions:
main.py: Main script that fetches data and saves it into CSV files.
users.csv: Stores data for users in London with over 500 followers.
repositories.csv: Stores details of the public repositories for these users.
README.md: Project documentation file.


Limitations and Recommendations:

Rate Limiting: If rate limits are hit often, consider implementing a longer delay between requests or breaking the requests into smaller batches.
Company Name Standardization: Company names may have varied formatting; consider additional cleanup rules if deeper analysis is required.
Recommendations for Developers:
Growing a GitHub presence requires consistent contributions, particularly to popular open-source repositories.
Active involvement in projects that have frequent updates and many contributors may also attract followers.
