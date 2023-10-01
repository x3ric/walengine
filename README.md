<div align="center">
   
### Walengine

Walengine is a unique web browser based on Surf, a lightweight GTK and WebKit-powered web browser.

### Features

**Browser Background**: Use your web browser as a background.

### To install on arch

<pre>
curl -s https://raw.githubusercontent.com/X3ric/walengine/main/install | bash
</pre>

### To install on others

<pre>
git clone https://github.com/x3ric/walengine
cd walengine
make
sudo make install
</pre>

<details>
<summary><h3>BlackScreen?</h3></summary>

to fix add  ```alias walengine='WEBKIT_DISABLE_COMPOSITING_MODE=1 walengine'``` to your shell.

this appends in some nvidia gpu.

</details>

</p><a href="https://archlinux.org"><img alt="Arch Linux" src="https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=D9E0EE&color=000000&labelColor=97A4E2"/></a><br>
