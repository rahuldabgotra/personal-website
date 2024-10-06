---
title: "About Me"
ShowBreadCrumbs: false
draft: false
---

{{< rawhtml >}}
<style>
  /* Style for the two-column layout */
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  .text-column {
    flex: 1;
    padding-right: 20px;
  }
  .image-column {
    flex: 0 0 200px;
    display: flex;
    text-align: center;
  }
  .image-column img {
    border-radius: 50%;
    width: 200px;
    height: 200px;
  }
  /* Responsive layout for smaller screens */
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
    .image-column {
      order: -1;
      text-align: center;
      margin-bottom: 10px;
    }
    .text-column {
      padding-right: 0;
      text-align: left;
    }
  }
</style>
<div class="container">
  <!-- Text Column -->
  <div class="text-column">
    <p>Hello, I’m <strong>Rahul Dabgotra</strong>, a Backend Developer from Jammu, J&K, India. I love transforming ideas into scalable applications and solving real-world challenges with innovative solutions. With expertise in <strong>Java</strong> and <strong>Spring Boot</strong>, I have successfully developed APIs, orchestrated cloud infrastructure, and built robust applications that deliver results.</p>
    <p>I am constantly exploring new technologies, and this website is where I share my experiences, insights, and exciting projects. I believe in continuous learning, and my blogs reflect my journey in tech.</p>
  </div>
  <!-- Image Column -->
  <div class="image-column">
    <img src="https://media.licdn.com/dms/image/v2/D5603AQF0B9GImG8D9g/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1728210434173?e=1733961600&v=beta&t=Ra-Mp6A_-BU6fw_1mw4_E1pd0EqszMWp_vJSW9eRMr4" alt="Picture of me">
  </div>
</div>
{{< /rawhtml >}}

---

## Project in Development

### Book Loop

 A social app for book lending and borrowing, **Book Loop** allows users to:

- Register and authenticate securely with JWT
- Manage books through a CRUD system
- Borrow and return books with approval workflows

**What I’ve implemented**:

- Developed a responsive frontend using **Angular** and **Bootstrap**.
- Built a secure backend with **Spring Boot 3** and **Spring Security 6** for JWT-based authentication.
- Integrated **Keycloak** for role-based authorization.
- Used **Docker** for seamless application deployment, with **GitHub Actions** for CI/CD.
  
You can explore the full project <a href="https://github.com/rahuldabgotra/book-loop-app" target="_blank" rel="noopener noreferrer">here</a>.

---

## Interested Areas

- **API Development**: Building efficient and secure APIs
- **Backend Optimization**: Improving performance and reliability
- **Cloud Infrastructure**: Deploying scalable cloud solutions
- **Exploring New Technologies**: From machine learning to blockchain

---

## Connect With Me

I'm always open to discussing technology, projects, and potential collaborations. Feel free to reach out to me via the following channels:

- [Twitter](https://x.com/rahuldabgotraa)
- [LinkedIn](https://www.linkedin.com/in/rahuldabgotra/)
- [GitHub](https://github.com/rahuldabgotra)
- [Email Me](mailto:rahuldabgotra@gmail.com)
