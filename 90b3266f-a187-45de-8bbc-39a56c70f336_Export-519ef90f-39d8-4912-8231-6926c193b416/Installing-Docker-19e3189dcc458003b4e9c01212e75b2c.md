# Installing Docker

Created: February 18, 2025 3:33 AM
Tags: Finished

[Following this guide to install docker on macOS](https://docs.docker.com/desktop/setup/install/mac-install/)

There are two versions to install docker because of the new Apple CPU chips in newer Mac computers. My computer uses an Intel chip so I will go with that dmg package.

![Screenshot 2025-02-18 at 4.02.24 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_4.02.24_AM.png)

This is the first build that Dockerdocs walks us through. It builds a small to-do application that runs on the local host, and they show us how api works for the greetings. Not entirely sure how api’s work but this is really interesting! They program the text to randomize from whatever is written in the list. As you can see in the text editor window, I took the liberty to add my own prompt. 

![Screenshot 2025-02-18 at 4.11.40 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_4.11.40_AM.png)

They also showed us how to edit the placeholder text within the text box. This did not require the page to be reloaded as when you save the file it will automatically change in the browser!

![Screenshot 2025-02-18 at 4.14.58 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_4.14.58_AM.png)

Then we changed the color of the site through the scss file.

![Screenshot 2025-02-18 at 4.29.15 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_4.29.15_AM.png)

I also took some time to play around with gradients since we were on the topic.

[I used this site to learn how to adjust the background color](https://docs.gerillass.com/docs/linear-gradient/)

- It is noted in the guide that the site responds immediately because it was loaded in a containerized environment, which means that the environment is constantly monitoring the files and applying whatever changes occur. This applied to the color gradients that I implemented.

---

# Building and Pushing the Image

![Screenshot 2025-02-18 at 5.14.50 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_5.14.50_AM.png)

![Screenshot 2025-02-18 at 5.15.19 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_5.15.19_AM.png)

Dockerdocs walks through how to push a build to the repository through terminal commands.

1. We have to clone the copy of the todo app that we created so that we can build an image of it to push to the repository.
2. Build the image. This will create the image for us to push to the repository.
3. I created a repository on the dockerhub so that I have a place to push the image to.

1. By writing
    
    ```bash
    docker image ls
    ```
    
    ![Screenshot 2025-02-18 at 5.19.41 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_5.19.41_AM.png)
    
    We can see the image that we created and can now push the image to the repository
    
2. Finally, by writing
    
    ```bash
    docker push [username]/getting-started-todo-app
    ```
    
    We push the image to the repository as seen in the screenshot below.
    
    ![Screenshot 2025-02-18 at 5.24.37 AM.png](Installing%20Docker%2019e3189dcc458003b4e9c01212e75b2c/Screenshot_2025-02-18_at_5.24.37_AM.png)
    

It also looks like there’s an option to pull the image from the repository. From my current understanding this seems like snapshots in Minecraft that provides a certain version or build of the game.

Overall, this process was very interactive and full of lessons. I understand how repositories work a little better now, how building and pushing images work. 

This build that I created during this guide can be seen [here](https://hub.docker.com/r/videshbridgelal/getting-started-todo-app)