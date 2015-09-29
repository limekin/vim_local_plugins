# Local plugins for Vim
This is a method I use to have project specific or local settings/plugins for the Vim editor. It's done by keeping a git ignored `vim_local.vim` file inside your project's root directory, and then defining your own project specific settings inside the file along with the scripts/plugins you want the project to use. An example `vim_local.vim` file you can use :

    source $HOME/.vim_scripts/to_haml.vim
    source $HOME/.vim_scripts/html_helpers.vim
    
    set path+=assets/sass
  
I also use a wrapper bash script (I named it `gvimm`) to hide the use of the local file like this :
  
    gvim -S ./vim_local.vim $*
    
So with the help of the wrapper I can simply call `gvimm file_to_edit` and the local vim settings will be picked up from the local vim settings file.
  
    
