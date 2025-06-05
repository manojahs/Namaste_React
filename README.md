```
# Namaste_React

<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
This is the core element of React
Example:
React.createElement("h1",{},"Namaste")

<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
This is the DOM create a root and render all the element to Root
example:
ReactDOM.createRoot("root")

crossorigin is helpful for getting When a browser requests a resource from a different domain (e.g., CDN), it’s considered a cross-origin request.

//  <div id="parent">
//     <div id="child">    
//         <h1></h1>
//     </div>
//  </div>
 
 
 App.js
--------------
 const header = React.createElement(
       "div",{ id: "parent" },
       React.createElement(
           "div",{id:"child"},
           React.createElement("h1", {}, "I am h1 tag"))
   );

   const root = ReactDOM.createRoot(document.getElementById("root"));
   root.render(header);

Here header is the React Element which is will create the object and once u call the render it will converts it to HTML

NPM is repo for all the packages
package.json is the configuration for npm

npm install -D parcel

| Purpose            | Command                 | Saved In          |
| ------------------ | ----------------------- | ----------------- |
| Dev Dependency     | `npm install -D parcel` | `devDependencies` |
| Regular Dependency | `npm install parcel`    | `dependencies`    |

You said:
remote: Permission to manojahs/Namaste_React.git denied to ManojHunachigi777.
fatal: unable to access 'https://github.com/manojahs/Namaste_React.git/': The requested URL returned error: 403


ChatGPT said:
The error you're seeing:

vbnet
Copy
Edit
remote: Permission to manojahs/Namaste_React.git denied to ManojHunachigi777.
fatal: unable to access 'https://github.com/manojahs/Namaste_React.git/': The requested URL returned error: 403
means that your GitHub user (ManojHunachigi777) does not have the required permission to push or access the repository owned by manojahs.

Here's how to resolve it:
✅ Option 1: Get Access from Repository Owner
If you are supposed to push to that repository:

Ask the owner (manojahs) to add you as a collaborator:

Go to the repository on GitHub.

Click Settings > Collaborators and teams > Add people.

Add ManojHunachigi777 with the appropriate permissions (write/admin).

Accept the invitation in your GitHub notifications.

Then try pushing again.

✅ Option 2: Use SSH instead of HTTPS (if you have access)
If you do have access but are using HTTPS and it's causing issues, switch to SSH:

Step 1: Make sure you have SSH set up
bash
Copy
Edit
ssh-keygen -t ed25519 -C "your_email@example.com"
Then add your public key (~/.ssh/id_ed25519.pub) to your GitHub account under Settings > SSH and GPG keys.

Step 2: Change the remote URL:
bash
Copy
Edit
git remote set-url origin git@github.com:manojahs/Namaste_React.git
Then try pushing again:

bash
Copy
Edit
git push origin main
✅ Option 3: Fork the repository
If you don’t need to push to manojahs/Namaste_React.git and just want to work on your own copy:

Go to: https://github.com/manojahs/Namaste_React

Click Fork.

Clone your fork and push there:

bash
Copy
Edit
git clone https://github.com/ManojHunachigi777/Namaste_React.git
Let me know what you're trying to do — push to someone else's repo, or work on your own version — and I can guide you step-by-step.






You said:
why its taking ManojHunachigi777 this user i need to push it to manojahs account


ChatGPT said:
You're getting the error because Git is using the credentials of the ManojHunachigi777 GitHub account on your system. To push to manojahs’s repository, your machine needs to authenticate as the manojahs user — the one that owns the repository.

🔧 How to Fix It
✅ Step 1: Check current GitHub account in VS Code
Run this in VS Code terminal or your shell:

bash
Copy
Edit
git config --global user.name
git config --global user.email
That only sets the name/email in commits — but GitHub authentication is based on the account that is logged in via Git credentials or GitHub CLI.

✅ Step 2: Clear stored GitHub credentials
You likely have cached credentials for ManojHunachigi777.

On Windows:

Search for Credential Manager in the Start Menu.

Go to Windows Credentials.

Look for any entries like:

git:https://github.com

or anything containing github.com

Remove them.

✅ Step 3: Re-authenticate with the correct GitHub account
Next time you push or pull from GitHub, Git will prompt for login. Make sure to log in as manojahs.

Or, to be safe, re-authenticate manually using GitHub CLI:

bash
Copy
Edit
gh auth login
Choose GitHub.com

Choose HTTPS

Authenticate with browser

Select the manojahs account

If gh (GitHub CLI) is not installed, download it from: https://cli.github.com/

✅ Step 4: Ensure the correct remote URL
Check your remote:

bash
Copy
Edit
git remote -v
If it's using HTTPS, you can keep it or switch to SSH (recommended for pushing):

To switch to SSH (must have SSH key added in GitHub):

bash
Copy
Edit
git remote set-url origin git@github.com:manojahs/Namaste_React.git
✅ Final Push
Now try pushing again:

bash
Copy
Edit
git push origin main
Let me know if you want help checking your current Git user session or switching between multiple GitHub accounts cleanly.






You said:
npm install -D parcel so ths is for dev dependncy how u ll give for normal dependenduc?


ChatGPT said:
You're absolutely right — npm install -D parcel installs Parcel as a dev dependency (the -D flag is shorthand for --save-dev).

✅ To install a regular (production/runtime) dependency, just omit -D:
bash
Copy
Edit
npm install parcel
This installs parcel as a regular dependency and saves it in the "dependencies" section of your package.json file.

📦 Summary
Purpose	Command	Saved In
Dev Dependency	npm install -D parcel	devDependencies
Regular Dependency	npm install parcel	dependencies

Let me know if you also want the same explained for yarn or pnpm.

Parcel is a web application bundler that automatically compiles and bundles your JavaScript, HTML, CSS, and other files into optimized output for the browser.








```

