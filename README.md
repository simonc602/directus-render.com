Full credit to the original author: https://github.com/directusbr/render

This guide is an English translation to help you get your Directus instance set up on Render.com. I've adapted the template to mirror an already existing external Supabase database (versus the original Directus db), you can see this in the .yaml file.

## Simplified Deployment with Render.com

With Directus, we've simplified the deployment process for you. Our quick deploy button on Render.com allows you to start a fully functional Directus environment with just one click. No complicated setup or advanced hosting knowledge is required. With this convenience, you can start managing your content and data effectively without worrying about server configuration complexities. Follow the instructions to deploy.

[Video on YouTube](https://youtu.be/Q-vpcxpnKog)


## What is Directus and what is it for?

Directus is a tool that helps manage information and content on a website, application, or online project. It’s like an organized system that allows you to easily enter, edit, and organize information, even if you're not a programmer.

### What is it used for?

Directus is used for:

- **Content Management:** With Directus, you can add, edit, and delete texts, images, videos, and other types of information on your website or application. This is useful for keeping your content up to date.

- **Layout Customization:** Even without knowing how to program, you can adjust how your website or application is displayed. You can change the design, colors, and organization of the information.

- **Access Control:** You can decide who can view and edit the information in your project. This is important to protect sensitive data and share information only with the right people.

- **Creating Forms:** If you need forms to collect information from your website visitors, Directus makes it easy to create them.

- **Integration with Other Tools:** Directus is a highly versatile platform that allows seamless integration of your website or application with a variety of tools and services, including social media authentication systems and external databases.

- **Maintaining a History:** Directus logs all the changes you make, so if something goes wrong, you can easily revert to an earlier version.

In summary, Directus is like an assistant that helps you manage and update your website or application, even if you don’t know how to code. It’s a useful tool for anyone who wants full control over their online content without needing advanced programming skills.

## Directus: A Technical Overview

Directus is an open-source content management system (CMS) that operates as an abstraction layer over a relational database. The primary technical feature of Directus is its ability to expose any SQL database as a RESTful API. Let’s dive into the key components and technical concepts that define Directus:

### Customizable RESTful API

- Directus offers a fully customizable RESTful API that allows developers to create, read, update, and delete (CRUD) data in the underlying database using HTTP requests.
- This API is highly configurable, enabling developers to expose only the resources and endpoints necessary to meet the needs of their applications.

### Admin Interface

- Directus provides a web-based admin interface that allows administrators and editors to easily manage the application's content.
- This interface is fully customizable and can be tailored to meet the specific workflow requirements of a project.

### Granular Access Control

- Directus offers granular access control based on roles, allowing developers to define which users or groups of users have permission to access, read, or modify certain resources.
- This is essential for ensuring data security and integrity.

### Custom Fields and Relationships

- Developers can define custom fields and complex relationships between data in Directus.
- This allows the creation of customized data structures to meet the specific needs of a project.

### Integrations and Extensibility

- Directus is highly extensible and supports integrations with other tools and services, making it a versatile choice for various development scenarios.
- Developers can create custom plugins and use hooks to further extend Directus’s functionality.

### Content Versioning

- Directus maintains a complete history of all changes made to the data, making it easy to audit and recover previous versions if needed.

### Flexible Hosting and Deployment

- Directus can be deployed in various environments, from local servers to cloud services.
- It supports multiple SQL database options, such as MySQL, PostgreSQL, and SQLite.

In summary, Directus is a powerful content management tool that provides a highly customizable RESTful API for accessing, manipulating, and managing data in a relational database. Its flexibility, granular access control, and customization capabilities make it an attractive choice for developers looking to create custom applications and websites with robust content management capabilities.

## Steps to Deploy:

### Fork the Repository:
- Fork the repository on GitHub where this YAML file is located.

### Connect GitHub to Render:
- Log in to your Render.com account and connect it to your GitHub account.

### Create a New Blueprint:
- Click on "New" -> "Blueprint" and select your forked repository / copy in the public github address.

### Select Branch:
- Choose the branch with the render.yaml file. By default, this is usually the main branch.

### Deploy:
- Render will automatically read the render.yaml file and start deploying your service. It will also set up the database and link it to your Directus instance.

### Access Your Directus Instance:
- Once the deployment is complete, you can access your Directus instance using the provided URL from Render.

### To Mirror Your Supabase Database (or other database)
- Go to your deployment in Render.com
- Set up environment variables: (For sensitive information like database credentials, it's better to use Render's environment variables rather than hardcoding them in the YAML file.)
- Go to your Supabase or Other Database dashboard and find credentials to link the two accounts. 
- For example, add your Supabase database credentials under the following keys:
  - DB_HOST
  - DB_PORT
  - DB_DATABASE
  - DB_USER
  - DB_PASSWORD

This configuration should successfully deploy Directus on Render.com with minimal manual setup.
