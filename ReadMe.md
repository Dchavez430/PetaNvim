Configuration for Nvim

# neovim-config

This is just a copy of my NeoVim configuration so I can easily share it with others. Feel free to use as-is, modify it, or just mine it for ideas.
It requires:
- NeoVim -- it may *kind of* work with Vim.
- vim-plug for plugin management.
- a bunch of vim plugins.
- a NerdFont to display correctly (it assumes Meslo NF in GUI mode).
- probably makes some other assumptions that I'm forgetting.

Known issues:
- The custom foldmethod is great, but sometimes does weird things. If this happens, just use ":set foldmethod=marker" or whatever you want on the fly.
- Probably some other little things, see the TODOs and FIXMEs in the code.

NVIM:  
	-Download NeoVim
	-It is a good idea to update the repository. If you dont you may get weird errors such as "no option camel"
	'sudo add-apt-repository ppa:neovim-ppa/stable'
	'sudo apt install neovim'
	make the directory if necessary
	'sudo cp _config/nvim/nvim.init .~/.config/nvim/init.vim'	
	'cp _config/_local/share/nvim -r /home/%(USER)/.local/share/'
	make the directory if necessary  
	'cp _config/_local/share/nvim/site/autoload/vim-plug/plug.vim -r /home/%(USER).local/share/nvim/site/autoload/plug.vim    
	run nvim, you will get plugin in errors, we are fixing that now  
	nvim  
		:PlugInstall  
		:UpdateRemotePlugins  
		:q!  

	Add the contents of _bashrcAddon.txt to the VERY END of your ~/.bashrc  or /home/$USER/.bashrc file  
	cat _bashrcAddon.txt | tee -a ~/.bashrc
	cat _bashrcAddon.txt | tee -a /home/$USER/.bashrc
