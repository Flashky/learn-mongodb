# Download

We will work using the Free Community Server Edition:

https://www.mongodb.com/try/download/community

# Installation

Follow the installation steps.

For Windows, install it as a **Network Service**.

Official documentation:

- [Windows](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
- [macOS](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)
- [Linux](https://docs.mongodb.com/manual/administration/install-on-linux/)

# Environment variables configuration

In order to use **mongo** and **mongod" commands from any folder, we need to add the bin folder to the **PATH** environment variable.

## Windows

Folder must be located somewhere such as ``C:\Program Files\MongoDB\Server\4.4\bin``.

How to add:

1. Press Windows key.
2. Type **env** and select **Edit the system environment variables**.
3. Click the **Environment Variables...** button.
4. Edit the **PATH** environment variable and click on **Edit...**.
7. Add the mongodb bin path to the list of environment variables.

## Unix / Mac

We will need to edit the .bash_profile file and add a line such as:

```bash
export PATH=<the_bin_folder>:PATH
```






