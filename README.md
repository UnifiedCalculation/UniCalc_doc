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

**Always make sure to keep MikTex updated!**

After installing these 3 components, you can download the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) plugin for VSC. This one will help you with highlighting, compiling etc.

To compile a *.tex file, hit **alt+ctrl+b**!

You can find a template *.tex file in the following [folder](https://github.com/UnifiedCalculation/UniCalc_doc/tree/master/Template%20File)