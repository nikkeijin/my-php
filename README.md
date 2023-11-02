# Seamless Solution for Designer to WordPress Theme Developer Handover

This PHP project architecture is tailored to meet the needs of companies with distinct role assignments, where a designer excels in HTML and CSS, while a dedicated PHP developer specializes in crafting WordPress themes. If your company has such a dynamic, this project architecture is the perfect solution.

Designed to resemble the WordPress architecture, this project facilitates a more seamless coding experience for designers proficient in HTML and CSS. The reason for this efficiency lies in the use of similar functions to those employed by WordPress, enabling a smoother transition and adaptation to the WordPress theme structure, facilitating the handover from designers to WordPress theme developers once the designer finishes coding with HTML and CSS.
    
## Project Structure

The project structure consists of several components and functions:

### Page Routing Methods

The `page_router()` function is responsible for routing requests to the appropriate PHP file based on the URL. This architecture includes management of the default front page when the URL is set to '/'.

### Template Directory Methods

- `get_template_directory_uri()`: This function defines the template directory's URI.

- `get_template_part($path)`: Use this function to include a specific template part from the template directory.

- `esc_url($url)`: A utility function for escaping URLs to prevent security vulnerabilities.

- `home_url($page_slug = '')`: Generate the URL for the home page or a specific page based on the given slug.

Example of the esc_url and home_url functions: `<a href="<?= esc_url(home_url('portfolio')); ?>">Portfolio</a>`

### Page Methods

- `is_front_page()`: Determine whether the current page corresponds to the front page.

- `is_page($page_slug)`: Determine if the current page matches a specific page slug.

## Usage

To run this project, we use Docker with a `docker-compose.yml` configuration. Follow these steps to get the project up and running:

1. Clone this repository to your local machine:
```bash
git clone https://github.com/yourusername/your-project.git
```

2. Ensure you have Docker and Docker Compose installed on your system, then navigate to the project directory:
```bash
cd your-project
```

3. Start the project using Docker Compose:
```bash
docker-compose up -d
```

You can access your project in a web browser by navigating to http://localhost.

The docker-compose.yml file includes configurations for Apache, MySQL, and phpMyAdmin. Additionally, the Dockerfile enables mod_rewrite for the Apache web server.

Please note that you can adjust the Docker configurations in the docker-compose.yml and Dockerfile to suit your specific needs.

Happy coding!
