# README.md

- **Data Collection**: Using the GitHub API, we extracted user data from Stockholm, focusing on users with over 100 followers and their top repositories.
- **Interesting Finding**: Users in Stockholm predominantly use languages like JavaScript and Python, with a surprising amount of well-maintained repositories in niche languages.
- **Recommendation**: Developers should consider enabling projects and wikis in repositories, as these features improve engagement and documentation clarity.

## Project Overview

This project uses the GitHub API to gather data on users in Stockholm with over 100 followers, as well as their repositories. The dataset includes user details and up to the 500 most recently pushed repositories for each user, providing a comprehensive look at Stockholm's GitHub community.

### Files in the Repository

1. **users.csv**: Contains user details, including login, name, company, location, email, and more.
2. **repositories.csv**: Lists each user's public repositories, including details such as full repository name, stargazers, watchers, and programming language.
3. **data_loading.ipynb**: Contains the code used for loading and processing data.
4. **data_analysis.ipynb**: Contains the data analysis code, which cleaned and structured the data.

### Data Fields

#### `users.csv`

- **login**: GitHub user ID
- **name**: Full name
- **company**: Cleaned and standardized company name
- **location**: User's city
- **email**: Email address
- **hireable**: Open to hire (true or false)
- **bio**: Short user bio
- **public_repos**: Number of public repositories
- **followers**: Number of followers
- **following**: Number of users they follow
- **created_at**: Account creation date

#### `repositories.csv`

- **login**: User ID
- **full_name**: Full repository name
- **created_at**: Repository creation date
- **stargazers_count**: Number of stars
- **watchers_count**: Number of watchers
- **language**: Primary programming language
- **has_projects**: Projects feature enabled (true or false)
- **has_wiki**: Wiki feature enabled (true or false)
- **license_name**: Repository license name

### Analysis Approach

1. **Data Collection**: The code first queried the GitHub API for users in Stockholm with over 100 followers, and retrieved each user's public repositories.
2. **Data Cleaning**: Company names were trimmed, capitalized, and stripped of leading `@` symbols. Missing values were standardized.
3. **Data Storage**: Structured data was saved into CSV files for user and repository information, maintaining data consistency and clarity.

### Observations and Recommendations

In analyzing the dataset, we noticed a tendency for Stockholm-based developers to prioritize certain languages and features in their projects. Developers are encouraged to enable both the Projects and Wiki features in their repositories, as these have proven to enhance project engagement.
