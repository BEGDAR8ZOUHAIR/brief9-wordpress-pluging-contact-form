Step 1 – Storing the Plugin

The first step to creating a new plugin is to make a folder for its files. The folder’s name should be unique and descriptive. Check the other plugin folders’ names within /wp-content/![Screenshot 2022-05-26 151934](https://user-images.githubusercontent.com/93929557/170508884-71dc488d-5cee-48db-83c9-076ff5cadfa6.png)
![Screenshot 2022-05-26 151952](https://user-images.githubusercontent.com/93929557/170508889-77276652-7e62-476b-bae0-8b771e6fafdd.png)
![Screenshot 2022-05-26 152025](https://use![Screenshot 2022-05-26 151835](https://user-images.githubusercontent.com/93929557/170508908-2adc24d8-507b-45fd-9858-db25922cc1be.png)
r-images.githubusercontent.com/93929557/170508890-8bf16228-ec11-4fa7-bf1b-6782488ec6f1.png)
plugins/ to make sure that the new name isn’t in use already.

Use an FTP client to connect to your hosting account to facilitate the file upload process. Navigate to wp-content -> plugins from the main WordPress directory. Then, create a new folder named my-first-plugin in the plugins folder.

Step 2 – Creating the First File

The main plugin file will contain the information WordPress requires to display your plugin in the plugin list where you’ll be able to activate it.

Create a new PHP file called my-first-plugin.php in the folder you made earlier. This main plugin file will contain header comments with additional information for WordPress to read or display.
You can refer to this PHP manual to understand why the closing tag ?> isn’t necessary here.

Save the file. Then, navigate to the Plugins section of your WordPress dashboard. If WordPress has read the new file correctly, you’ll see My First Plugin on the list


Step 3 – Writing the Plugin Functions
Before we begin writing the functions for the plugin, it is highly recommended to give all files, functions, and variables a unique prefix in their name to avoid any conflicts with other plugins. In our example, we’ll be using the prefix mfp, which is short for My First Plugin.

Create a new folder named Includes in the plugin’s main directory. We’ll use it to store supporting files used by the main file. In this folder, create a PHP file and name it mfp-functions.php. Give it the opening <?php tag on the first line.

This new file will contain all of your plugin’s functions.

We’ll have to include mfp-functions.php in the main plugin file to allow the other plugin files to use the functions it defines. Use require_once to ensure the plugin only works if the functions file is present.

Edit my-first-plugin.php as shown below. Then, save it and upload the file once again, overwriting the previous version when asked.
