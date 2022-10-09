# LINUX

<details><summary>Links</summary>
<p>
https://www.freecodecamp.org/news/git-cheat-sheet/

</p>
</details>

## GENERAL

<details><summary>Linux command line general tips</summary>
<p>

  <details><summary>Remove files starting with a dash</summary>
  <p>
    
  ```bash
  #Method 1
  rm -- --my-file.txt
  ```

  </p>
  
  <p>
    
  ```bash
  #Method 2
  rm ./--my-file.txt
  ```

  </p>
  </details>
</p>
</details>

## GNOME

<details><summary>Gnome related settings</summary>
<p>

  <details><summary>Display all buttons on menu bar</summary>
  <p>
    
  ```bash
  # The command gsettings can be used to change multiple gnome settings
  gsettings set org.gnome.desktop.wm.preferences button-layout 'appmenu:minimize,maximize,close'
  ```

  </p>
  </details>

  <details><summary>Disable gnome animations</summary>
  <p>
    
  ```bash
  gsettings set org.gnome.desktop.interface enable-animations false
  ```

  </p>
  </details>

  <details><summary>Watch for changes in gnome configuration</summary>
  <p>
    
  ```bash
  # Change the path to watch for specific settings - /org/gnome/desktop/interface
  dconf watch /
  ```

  </p>
  </details>

</p>
</details>
