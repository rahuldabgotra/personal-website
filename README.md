# Personal Website

This project is a personal website built using Hugo to share insights on various technologies, personal experiences, and showcase projects. It also allows contributions in the form of blog posts.

## Project Description

This website is designed to share my knowledge on technology and personal experiences, as well as act as a portfolio for my projects.  

- **Purpose**: To engage with a community by sharing content and to demonstrate my expertise through detailed project showcases.
- **Technology**: I chose Hugo for its speed and flexibility in creating static websites, along with GitHub Actions for automated deployment.
- **Challenges & Future Features**: Managing continuous content updates, exploring headless CMS integration, and improving SEO optimizations.

## Table of Contents

- [How to Install and Run the Project](#how-to-install-and-run-the-project)
- [How to Use the Project](#how-to-use-the-project)
- [How to Contribute](#how-to-contribute)
- [Badges](#badges)
- [License](#license)

## How to Install and Run the Project

### Prerequisites

- Install [Hugo](https://gohugo.io/getting-started/installing/) on your system.
- Ensure Git is installed.

### Steps to Install

1. **Clone the Repository**  
   Run the following command:

   ```bash
   git clone https://github.com/username/personal-website.git
   cd personal-website
   ```

2. **Run Hugo Locally**  
   Start the local development server:

   ```bash
   hugo server -D
   ```

   Open `http://localhost:1313` in your browser to view the website.

3. **Build for Production**  
   Generate the static files:

   ```bash
   hugo
   ```

## How to Use the Project

This website features a section to share blog posts under `/content/blogs/{year}/blogs`. It also includes a portfolio of my projects.  

- **Authentication**: None required for general users.
- **Visual Structure**: The site is styled using a simple, minimalistic theme for ease of reading and navigation.

Contributors can submit blogs or suggest changes to content by following the contribution guide.

## How to Contribute

We welcome contributions to blog posts or website improvements:

1. **Fork the repository**.
2. **Add a new blog post**:  
   Navigate to `/content/blogs/{year}/` and create a Markdown file for your blog post.
3. **Submit a Pull Request**:  
   After making changes, submit a pull request. Your contributions will be reviewed before merging.

### Contribution Guidelines

- Follow the Markdown structure for blog posts.
- Keep your content relevant and informative.

## Badges

![Hugo Version](https://img.shields.io/badge/Hugo-0.115.3-blue.svg) ![License](https://img.shields.io/badge/License-Apache%202.0-green.svg)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
