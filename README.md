# UniCalc_doc
Main repository for documentation of UniCalc


### Using LaTeX for the documentation

There is an easy way of using LaTeX on windows for the documentation. The following 3 Requirements have to be met:

- Install [VisualStudioCode](https://code.visualstudio.com/)
- Install [Perl](http://strawberryperl.com/)
- Install [MikTex](https://miktex.org/download)
- Link MikTex to tikz-uml-files:
   - Go to MiKTeX Console
   - Settings -> Tab Directories
   - Click the "+"
   - Add the folder "UniCalc_doc\Artefakte\tikz-uml files
   - User Guide can be found [here](https://perso.ensta-paris.fr/~kielbasi/tikzuml/var/files/html/web-tikz-uml-userguide.html)

**Always make sure to keep MikTex updated!**

After installing these 3 components, you can download the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) plugin for VSC. This one will help you with highlighting, compiling etc.

To compile a *.tex file, hit **alt+ctrl+b**!

You can find a template *.tex file in the following [folder](https://github.com/UnifiedCalculation/UniCalc_doc/tree/master/Template%20File)

### ERM for the database

Was built using draw.io and can be found [here](https://github.com/UnifiedCalculation/UniCalc_doc/blob/master/ERM.drawio)
To open it up go to draw.io and select GitHub as source.


### Domain model for the database

Was built using draw.io and can be found [here](https://github.com/UnifiedCalculation/UniCalc_doc/blob/master/Domain%20model.drawio)
To open it up go to draw.io and select GitHub as source.

### Wireframe for UI Design

The concepts for UI Design were made using PowerPoint and can be found here:
 - Mobile: https://1drv.ms/p/s!Ag4nu1H8FHKmiL8JGMsa0tJfaYjMTg?e=Z7gxg0
 - Desktop: https://1drv.ms/p/s!Ag4nu1H8FHKmiL8LyamVevU6AxBq1A?e=pzpJdi

## Development 

Development on UniCalc is done using [Trunk Based Development](https://trunkbaseddevelopment.com/).
What this means: 
**master** branch is always the "release" branch. Any Push to it means a stable release.
**development** branch is the active development branch. You can:
 - Commit directly to (works well if you are working alone on the project)
 - Create **short lived feature branches (1-2 days maximum)** and merge them back into development
 
To help with development, a choice of actions is used on every repository to help with managing everything. The idea here is to use GitHub Projects as a management tool for open tasks and issues. What this means:
- Tag issues in your commits (You can do so using #1, #2 according to the issue number), and GitHub will then automatically list them in the issue
- Use Milestones etc. to tag your work!

The following actions will be used to make life easier:
 - [Assignee to reviewer](https://github.com/marketplace/actions/github-action-for-assignee-to-reviewer): This action requests a review from the currently assigned person on a **Pull Request**. This means you create a Pull Request, assign it to someone, and this action will tag him, so that he can then review the PR. 
- [Create Issue Branch](https://github.com/marketplace/actions/create-issue-branch) This creates a new branch for an issue, as soon as someone is **either** assigned to the issue **or** comments with `/cib`.
- **pdfBackend**: Has a custom Action that runs maven tests, to make sure everything passes before being merged into master
- **frontend**: Has two custom Actions. The first one runs the usuall tests on a pull request. The second one handles copying the new components from the [fronted repository](https://github.com/UnifiedCalculation/UniCalc_Frontend) to the [backend repository](https://github.com/UnifiedCalculation/UniCalc_backend), as well as creating a new PR on it.

