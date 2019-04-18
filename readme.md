# Playing with Netlify CLI

How to setup your netlify site using only the Command Line Interface.

You will need to log into netlify when the website prompts you to after you type in:

```
netlify login
```

>For the purpose of this document **netlify101** is the name of the project. 
>For your project, replace **netlify101** with the name of your project.

Create a repository like this

```
git init netlify101
```

Create a file, or setup your project as  you normally do. 
After you have done the initial setup add the netlify setup.

```
netlify init
```

It will take you through a wizard, so just answer the questions. 
As part of the wizard it will ask you if you want to create a `netlify.toml` file. Select yes for that question.

**NOTE**

If you are making simple straight up HTML site without a generator, then put all those files in a folder called `_site` and in the **netlify.toml** file set the publish paramter to `_site` like this:

```
[build]
  publish = "_site"
```

The code above is the entire content of my `netlify.toml` file.

To check if you are happy with your setup, you can now check this live on your own device by doing:

```
netlify dev --live
```

You can now open the site on the url that is presented to you ending in `netlify.live`

Once you are happy with the site and check if your netlify configuration is ok type in the following to setup your remote site:

```
netlify deploy
```

Once that is done, the next time you push your site to your deploy branch, your netlify site will show it.

The cli will inform you of any errors, and also to use the `--prod` flag if you are happy with the product, so that your site can be live on your project URL

```
netlify deploy --prod
```

Finally to view the site in your browser type in:

```
netlify open:site
```

To view the admin panel in your browser type in:

```
netlify open:admin
```

**Extra Links:**

* [https://www.netlify.com/docs/netlify-toml-reference/](https://www.netlify.com/docs/netlify-toml-reference/)

* [https://cli.netlify.com](https://cli.netlify.com)

**Site Preview**

The site is a single line of HTML, but still a reference to this readme :smile:

* [https://netlify101.netlify.com](https://netlify101.netlify.com)