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

## Personal Access Tokens (PATs) UI
The inspector includes a UI for managing Personal Access Tokens (PATs) for authenticated users or on behalf of other users (e.g., technical / service users).

### Usage
- Open User Management in the Inspector.
- On the **Users** page, open the user actions dropdown menu:
  - Select **PATs** to view and manage existing tokens for that user.
- Alternatively, navigate to the **PATs** tab and click **Create** to open the token creation dialog.
- Optionally enter or adjust the **Username** if creating a token on behalf of another user.
- Enter a **Token Name**, choose validity duration and unit (days, months, or years), and optionally select a subset of roles and privileges.
- Click **Save** to generate the token, then copy and store the generated token string.

### REST API
- `GET /rest/strolch/privilege/tokens`: Fetches PATs for the authenticated user (or with `?username={username}` for another user).
- `POST /rest/strolch/privilege/tokens`: Creates a new PAT (accepts optional `username` in JSON body).
- `DELETE /rest/strolch/privilege/tokens/{tokenId}`: Revokes a PAT.
