# CI-User-Auth

## Description
CI-User-Auth is a PHP CodeIgniter module for user authentication. It provides features like registration, login, password reset, and session management.

## Installation
1. Clone the repository: `git clone https://github.com/your-username/CI-User-Auth.git`
2. Configure your CodeIgniter application to autoload the `Auth_model`.
3. Customize the module according to your application's requirements.

## Usage
```php
// Load the Auth_model
$this->load->model('Auth_model');

// Register a new user
$user_data = array(
    'username' => 'example_user',
    'email' => 'user@example.com',
    'password' => 'secure_password'
);
$user_id = $this->Auth_model->register_user($user_data);

// Login a user
$username = 'example_user';
$password = 'secure_password';
$login_successful = $this->Auth_model->login_user($username, $password);

// Reset user password
$email = 'user@example.com';
$password_reset_successful = $this->Auth_model->reset_password($email);

// Logout user
$this->Auth_model->logout_user();
