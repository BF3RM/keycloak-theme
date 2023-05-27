# Reality Mod Keycloak Theme

This is a Keycloak theme designed for the BF3: Reality Mod community. The theme is based on the default Keycloak theme and has been customized to match the visual style of the BF3: Reality Mod.

## Installation

1. Clone the repository: `git clone https://github.com/BF3RM/keycloak-theme.git`
2. Copy the `realitymod` directory to the Keycloak themes directory: `cp -r realitymod /path/to/keycloak/themes`
3. Restart Keycloak to load the new theme.

## Usage

1. Log in to the Keycloak admin console.
2. Go to the Realm Settings for the realm you want to apply the theme to.
3. Select the `Themes` tab.
4. Select `realitymod` from the `Login Theme` dropdown.
5. Save the changes.

The BF3: Reality Mod theme should now be applied to the login page for the selected realm.

## Development

Start the development environment by running `docker-compose up`. This will start a PostgreSQL database and a Keycloak instance with the theme mounted in the themes directory. The Keycloak instance will be available at `http://localhost:8080`.

Go to the admin console at http://localhost:8080/auth/admin and log in with the username `admin` and password `admin`. After that go to the `Realm Settings` for the `master` realm and select the `realitymod` theme from the `Login Theme` dropdown. Save the changes and the theme should be applied to the login page.

### Coding

Keycloak uses [Apache FreeMarker](https://freemarker.apache.org/) for templating and [Less](http://lesscss.org/) for styling. If your template does not render as expected, check the logs for errors. The logs can be found by running `docker-compose logs keycloak`. Changes to the files are immediately reflected on refresh. More information about theme development can be found [here](https://www.keycloak.org/docs/latest/server_development/#creating-a-theme).

The goal is to use as much as the original templates as this makes upgrading easier. It is therefor recommended to check both the `base` and `keycloak` themes [here](https://github.com/keycloak/keycloak/tree/main/themes/src/main/resources/theme). Those will give you a good understanding how the original template looks like and which properties are available.

## License

This theme is licensed under the [MIT License](LICENSE).
