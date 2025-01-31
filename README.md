
<p align="center">A modern, responsive and customizable portfolio builder for Developers!</p>
<p align="center">http://nscsp-it.github.io/nscsp-pf</p>




## 🛠 Installation & Set Up

These instructions will get you a copy of the project and deploy your website online!

  - **[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo)** the repo so you have your own project to customize by clicking the fork icon on the top right side. A "fork" is a copy of a repository.
  - Rename your forked repository to <code>username.github.io</code> in github, where <code>username</code> is your GitHub username (or organization name).
  - Go to your repo's **Actions** page and enable workflows.\
  ![Workflows](https://arifszn.github.io/assets/img/hosted/ezprofile/workflows.png)

  - Open <code>package.json</code>, and change <code>homepage</code>'s value to <code>https://username.github.io</code>.
  
    ```js
    // package.json
    {
      // ...
      "homepage": "https://username.github.io",
    }
    ```

  - Now commit to your **main** branch with your changes.
  - The CI/CD pipeline will publish your page at the gh-pages branch automatically.
  - Go to your repo's **Settings** -> **Pages** -> **Source** and change the branch to gh-pages and click **save**.
  - Your personal portfolio will be live at <code>username.github.io</code>.
  - Any time you commit a change to the **main** branch the website will automatically update.

  
You can skip the above steps and do a manual deployment by running <code>npm run deploy</code>. For more info, visit [here](https://create-react-app.dev/docs/deployment/#github-pages).

As this is a create react app, you can also host your website to Netlify, Vercel, Heroku, or other popular services. Please refer to this [doc](https://create-react-app.dev/docs/deployment) for a detailed deployment guide to other services.

If you see only <code>README</code> at <code>username.github.io</code>, be sure to change your GitHub Page's source to <code>gh-pages</code> branch. See [how to](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).



## 🎨 Customization

All the magic happens in the file <code>src/config.js</code>. Open it and modify it according to your preference.

These are the default values:

<details>
<summary>config.js</summary>

```js
// config.js
module.exports = {
  github: {
    username: 'arifszn', // Your GitHub org/user name. (Required)
    sortBy: 'stars', // stars | updated
    limit: 8, // How many projects to display.
    exclude: {
      forks: false, // Forked projects will not be displayed if set to true.
      projects: [] // These projects will not be displayed. example: ['my-project1', 'my-project2']
    }
  },
  social: {
    linkedin: '',
    twitter: '',
    facebook: '',
    dribbble: '',
    behance: '',
    medium: '',
    devto: '',
    website: '',
    phone: '',
    email: ''
  },
  skills: [
    'JavaScript',
    'React.js',
  ],
  experiences: [
    {
      company: 'Company name 1',
      position: 'Software Engineer',
      from: 'July 2019',
      to: 'Present'
    },
    {
      company: 'Company name 2',
      position: 'Jr. Software Engineer',
      from: 'January 2019',
      to: ' June 2019'
    }
  ],
  education: [
    {
      institution: 'Institution name 1',
      degree: 'Bachelor of Science',
      from: '2015',
      to: '2019'
    },
    {
      institution: 'Institution name 2',
      degree: 'Higher Secondary Certificate (HSC)',
      from: '2012',
      to: '2014',
    }
  ],
  blog: {
    // Display blog posts from your medium or dev.to account. (Optional)
    source: 'dev.to', // medium | dev.to
    username: 'arifszn',
    limit: 5 // How many posts to display. Max is 10.
  },
  googleAnalytics: {
    // GA3 tracking id/GA4 tag id
    id: '' // UA-XXXXXXXXX-X | G-XXXXXXXXXX
  },
  hotjar: {
    id: '',
    snippetVersion : 6 
  },
  themeConfig: {
    default: 'light',

    // Hides the theme change switch
    // Useful if you want to support a single color mode
    disableSwitch: false,

    // Should we use the prefers-color-scheme media-query,
    // using user system preferences, instead of the hardcoded default
    respectPrefersColorScheme: true,

    // Available themes. To remove any theme, exclude from here.
    themes: [
      'light',
      'dark',
      'cupcake',
      'bumblebee',
      'emerald',
      'corporate',
      'synthwave',
      'retro',
      'cyberpunk',
      'valentine',
      'halloween',
      'garden',
      'forest',
      'aqua',
      'lofi',
      'pastel',
      'fantasy',
      'wireframe',
      'black',
      'luxury',
      'dracula'
    ]
  }
}
```
</details>


### Themes

There are 21 themes available that can be selected from the dropdown. 

The default theme can be specified.

```js
// config.js
module.exports = {
  // ...
  themeConfig: {
    default: 'light',
    // ...
  }
}
```

### Google Analytics

ezFolio supports both GA3 and GA4. If you do not want to use Google Analytics, keep the <code>id</code> empty.
```js
// config.js
module.exports = {
  // ...
  googleAnalytics: {
    id: ''
  },
}
```

Besides tracking visitors, ezFolio will track click events on projects and blog posts, and send them to Google Analytics.\
<br/>
![Event](https://www.arifszn.com/assets/img/hosted/ezprofile/event.png)

### Hotjar

ezProfile supports hotjar. If you do not want to use Hotjar, keep the <code>id</code> empty.

```js
// config.js
module.exports = {
  // ...
  hotjar: {
    id: '',
    snippetVersion : 6 
  },
}
```

### Meta Tags

Meta tags will be auto-generated from configs dynamically. However, you can also manually add meta tags in <code>public\index.html</code>


### Avatar and Bio

Your github avatar and bio will be displayed here.\
<br/>


### Social Links

ezProfile supports linking your social media services you're using, including LinkedIn, Twitter, Facebook, Dribbble, Behance, Medium, dev.to, personal website, phone and email.
```js
// config.js
module.exports = {
  // ...
      socaial: {
        linkedin: '',
        twitter: 'NscspI',
        facebook: 'NSCSP.US',
        dribbble: '',
        behance: '',
        medium: '',
        devto: '',
        website: 'https://nscsp-it.github.io',
        phone: '999-999-9999',
        email: 'nscspit@gmail.com'
  },
}
```


### Skills

To showcase your skills provide them here.
```js
// config.js
module.exports = {
  // ...
  skills: [
    'JavaScript',
    'React.js',
  ],
}
```

Empty array will hide the skills section.


### Experience

Provide your job history in <code>experiences</code>.
```js
// config.js
module.exports = {
  // ...
  experiences: [
    {
      company: 'Company name 1',
      position: 'Software Engineer',
      from: 'July 2019',
      to: 'Present'
    },
    {
      company: 'Company name 2',
      position: 'Jr. Software Engineer',
      from: 'January 2019',
      to: ' June 2019'
    }
  ],
}
```

Empty array will hide the experience section.


### Education

Provide your education history in <code>education</code>.
```js
// config.js
module.exports = {
  // ...
  education: [
    {
      institution: 'Institution name 1',
      degree: 'Bachelor of Science',
      from: '2015',
      to: '2019'
    },
    {
      institution: 'Institution name 2',
      degree: 'Higher Secondary Certificate (HSC)',
      from: '2012',
      to: '2014',
    }
  ],
}
```

Empty array will hide the education section.


### Projects

Your public repo from github will be displayed here automatically. You can limit how many projects do you want to be displayed. Also, you can hide forked or specific repo.

```js
// config.js
module.exports = {
  // ...
  github: {
    username: 'arifszn',
    sortBy: 'stars',
    limit: 8,
    exclude: {
      forks: false,
      projects: ['my-project1', 'my-project2']
    }
  },
}
```

### Blog Posts

If you have [medium](https://medium.com) or [dev.to](https://dev.to) account, you can show your recent blog posts in here just by providing your medium/dev.to username. You can limit how many posts to display (Max is <code>10</code>).

```js
// config.js
module.exports = {
  // ...
  blog: {
    source: 'dev.to',
    username: 'arifszn',
    limit: 5
  },
}
```
The posts are fetched by [Article-api](https://github.com/arifszn/article-api).

## 📄 License

ezProfile is licensed under the [Apache-2.0 License](https://github.com/arifszn/ezprofile/blob/main/LICENSE).
