# wpgtk.atom
<a href="https://github.com/GeoDerp/SwayWM_Build/edit/master/README.md"><img src="https://img.shields.io/badge/Main%20Repo-SwayWM_Build-red.svg?style=for-the-badge&logo="></a>
<a href="https://atom.io/"><img src="https://img.shields.io/badge/IDE-Atom-brightgreen.svg?style=for-the-badge&logo=Atom"></a>
<a href="https://github.com/deviantfero/wpgtk"><img src="https://img.shields.io/badge/package-wpgtk-red.svg?style=for-the-badge&logo="></a>
<a href="https://github.com/atom/one-dark-ui"><img src="https://img.shields.io/badge/UI%20theme-One%20Dark-brightgreen.svg?style=for-the-badge&logo=Atom"></a>

![Gif](https://raw.githubusercontent.com/GeoDerp/wpgtk.atom/master/thumbnails/fast.gif)

**Description**: Atom Colour schemes with wpgtk support  
**Note**: *Not the best, will likely add to/upgrade the themes down the tack*  


## Themes
**wpgtk-one-dark-ui** = An Hacked Version of Atom's [one-dark](https://github.com/atom/one-dark-ui) UI theme  
**wpgtk-theme-syntax** = An Basic generated Syntax Theme

## Installation 
**There are two different approaches of installing these themes:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*(Before implementing, make sure you have both [Atom](https://atom.io/) and [wpgtk](https://github.com/deviantfero/wpgtk) installed)*
  
### Approach one - *manually*  
  - simply *(after downloading the git repo)* manually drag the `wpgtk-one-dark-ui` &  `wpgtk-theme-syntax`  folders into the .atom dir (``~/.atom``).   
  - Then, drag the wpgtk Templates (*the base files in the templates' dir*) into  ``~/config/wpg/templates/ folder``.     
   
  - Open wpgtk (wpg) app and in *Templates Tab* readd the symlink for the two config files:     
    ``Templates Tab > Add > ``   
    ``~/.atom/packages/wpgtk-theme-syntax/styles/colors.less ``      
    ``~/.atom/packages/wpgtk-one-dark-ui/styles/ui-variables-custom.less`` 
  
  - Open Atom and set the theme via the "UI Theme & Syntax Theme " drop-down in the "Themes" tab of the Settings View <br/>
  
### Approach two - *command line (**Recommended**)*
  In your terminal of choice, Past the following lines:
  
  ```bash
  cd ~/
  git clone https://github.com/GeoDerp/wpgtk.atom
  mkdir -p ~/.atom/packages
  mkdir -p ~/.config/wpg/templates/
  mv ~/wpgtk.atom/templates/wpgtk-one-dark-ui_styles_ui-variables-custom.less.base ~/.config/wpg/templates/
  mv ~/wpgtk.atom/templates/wpgtk-theme-syntax_styles_colors.less.base ~/.config/wpg/templates/
  mv ~/wpgtk.atom/wpgtk-one-dark-ui ~/.atom/packages/
  mv ~/wpgtk.atom/wpgtk-theme-syntax ~/.atom/packages/
  # you may still have to enable the theme via the "UI Theme & Syntax Theme " drop-down in the "Themes" tab of the Settings View
  wpg --link ~/.config/wpg/templates/wpgtk-theme-syntax_styles_colors.less.base ~/.atom/packages/wpgtk-theme-syntax/styles/colors.less
  wpg --link ~/.config/wpg/templates/wpgtk-one-dark-ui_styles_ui-variables-custom.less.base ~/.atom/packages/wpgtk-one-dark-ui/styles/ui-variables-custom.less
  ln -s ~/.atom/packages/wpgtk-theme-syntax/styles/colors.less ~/.config/wpg/templates/wpgtk-theme-syntax_styles_colors.less
  ln -s ~/.atom/packages/wpgtk-one-dark-ui/styles/ui-variables-custom.less ~/.config/wpg/templates/wpgtk-one-dark-ui_styles_ui-variables-custom.less
  # optional, if you want to delete the root folder:
  sudo rm -r ~/wpgtk.atom
  
  ```

### Note:  
If you want Atom's theme to automatically change colours live you will have to run atom in **dev** mode. <br/>  
  > *"To open a Dev Mode Atom window run `atom --dev .` in the terminal, or use `the _View > Developer > Open` in Dev Mode_ menu. When you edit your theme, changes will instantly be reflected!"*  < 
[Creating a Theme. Retrieved from https://flight-manual.atom.io/hacking-atom/sections/creating-a-theme/](https://flight-manual.atom.io/hacking-atom/sections/creating-a-theme/)
<br/>  
   
**Welp**, I hope you like it :blush: :smiley:.
  Feel free to let me know if there are any improvements/changes you will like me to make :smile:.
  
*sincerely*,   
&nbsp;&nbsp;&nbsp;[**GeoDerp**](https://github.com/GeoDerp)
