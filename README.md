# Weblog
This is a Flask web application that serves as a simple blogging platform. It allows users to create, edit, and delete blog posts. The application uses Flask-WTF for form handling, Flask-CKEditor for a rich text editor to create blog posts, Flask-Bootstrap for styling, and Flask-SQLAlchemy to store blog posts in an SQLite database.

Here's a breakdown of the main functionalities of the application:

Home Page ("/"): Displays all existing blog posts stored in the database. Each post is shown with its title, subtitle, author, and a brief preview of its content. Users can click on a post to view its full content on a separate page.

Blog Post Page ("/post/int:post_id"): Shows the full content of a specific blog post based on the provided post ID. Users can access this page by clicking on a post from the home page. The post's title, subtitle, author, image, and complete content are displayed.

About Page ("/about"): A simple static page that provides information about the blog or the blog's author.

Contact Page ("/contact"): Another static page that can contain contact information or a contact form for users to get in touch with the blog's owner.

New Blog Post Page ("/new-post"): This page allows users to create a new blog post. The page contains a form with fields for the post's title, subtitle, author name, image URL, and content. The rich text editor provided by Flask-CKEditor allows users to format their blog posts using various styling options. Once the form is submitted, a new blog post is created and stored in the database, and the user is redirected to the home page to see all posts.

Edit Blog Post Page ("/edit-post/int:post_id"): This page is similar to the "/new-post" page, but it allows users to edit an existing blog post. The fields are pre-filled with the existing content of the selected post, and users can modify any part of the post. Once the edited post is submitted, the changes are saved in the database, and the user is redirected to view the updated post.

Delete Blog Post ("/delete/int:post_id"): This endpoint allows users to delete a specific blog post by providing its post ID. After deletion, the post is removed from the database, and the user is redirected to the home page.

The application follows the typical Flask structure, where each route is associated with a specific function that handles the corresponding page's logic. The application uses a single SQLite database to store blog posts, and the "BlogPost" model represents the structure of the posts with various attributes such as title, subtitle, date, body, author, and image URL.

Please note that this is a basic blogging platform and lacks features like user authentication, user registration, and pagination. Depending on the specific needs and requirements, additional features and improvements can be implemented in the application.
