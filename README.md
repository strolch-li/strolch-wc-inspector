# strolch-wc-inspector
Strolch WebComponent Inspector

## Configuration UI
The inspector now includes a UI for managing the Strolch configuration and policy model.

### Usage
- Open the Inspector.
- Select "Configuration" from the system menu.
- View and update the core Strolch configuration (environment, etc.).
- View and update the policy model mappings.

### REST API
The UI communicates with the following REST API endpoints:
- `GET /strolch/configuration/resource`: Fetches the current configuration.
- `PUT /strolch/configuration/resource`: Updates the configuration.
- `GET /strolch/configuration/policies`: Fetches the policy model.
- `PUT /strolch/configuration/policies`: Updates the policy mappings.
