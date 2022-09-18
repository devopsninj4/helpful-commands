# TMUX

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

Kill all sessions but the current
```bash
tmux kill-session -a
```
<space>\<space>
Kill all sessions but my-session
```bash
tmux kill-session -a -t my-session
```
</p>
</details>
