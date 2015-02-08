AQUI es el 10
===============

Here lives the frontend code (CSS & MD & images) for [aquiesel10.mx](http://aquiesel10.mx) (http://reddit.com/r/AquiEsEl10)

Links
=====
We work on 3 distinct wikis:
* The [Textos](https://github.com/wikipoliticamx/AquiEsEl10/wiki/Textos) page in the Github wiki.
* This titanpad: https://wikipolitica.titanpad.com/24
* The [subreddit wiki](https://www.reddit.com/r/AquiEsEl10/wiki/index)

[First mockup](https://moqups.com/wikipoliticamx/Btdy4CHx/p:a75808438). See also the screenshots folder.

Other Geekery
=============

Using this in my vimrc to have scss files automatically processed to css and copied to the clipboard on saving them:

```VimL
autocmd BufWritePost,FileWritePost *.scss call ProcessAndCopySCSS()
function ProcessAndCopySCSS()
	let scss = expand('%:p')
	exec "silent !sass --update " . scss
	let css = substitute(scss, "scss", "css", "")
	exec "silent !cat " . css . " | pbcopy"
endfunction
```

Installation Instructions
-------------------------

Step one: Setting up the sidebar
  1. Go to /r/AquiEsEl10/about/edit
  2. Paste `sidebar.md` in the sidebar textarea: 
  3. Scroll down more and under 'look and feel' click 'choose file' and upload the headerbypass.png.
  4. Hit save!

Step two: The CSS
  1. Go to /r/AquiEsEl10/about/stylesheet
  2. Paste the `AquiEsEl10.css` file into the css textarea.
  3. Upload the images from the /images/ folder - except the headerbypass one. (Don't rename them!)
  4. Hit save again!
