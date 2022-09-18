# TMUX

<details><summary>Links</summary>
<p>

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example.html

https://docs.aws.amazon.com/cli/latest/reference/ec2/create-vpc.html

https://brad-simonin.medium.com/create-an-aws-vpc-and-subnet-using-the-aws-cli-and-bash-a92af4d2e54b

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
