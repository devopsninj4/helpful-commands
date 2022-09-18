# TMUX

<details><summary>Links</summary>
<p>

https://www.linode.com/docs/guides/persistent-terminal-sessions-with-tmux/

</p>
</details>  
  

## Sessions

<details><summary>Create a new session</summary>
<p>
  
```bash
tmux
```
  
```bash
tmux new
```

```bash
tmux new -s my-session
```
</p>
</details>

<details><summary>Delete sessions </summary>
<p>
  
```bash
tmux kill-ses -t my-session
```
```bash
tmux kill-session -t my-session
```

```bash
tmux kill-session -a
```  

```bash
tmux kill-session -a -t my-session
```
</p>
</details>


## Panes

<details><summary>Disable/Enable panes</summary>
<p>
  
  PS: These commands must be executed within a tmux session

  
  
```bash
:select-pane -d
```
    
```bash
:select-pane -e
```

</p>
</details>
