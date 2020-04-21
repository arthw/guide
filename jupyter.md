### jupyter use conda env ###
conda install nb_conda_kernels

### two data in one figure 

```
fig, ax1 = plt.subplots()
t = bs_list
color = 'tab:red'
ax1.set_xlabel('BS')
ax1.set_ylabel('Troughput', color=color)
ax1.bar(t, throughputs, color=color)
ax1.tick_params(axis='y', labelcolor=color)

    
ax2 = ax1.twinx()
color = 'tab:blue'
ax2.set_ylabel('Latency', color=color)
ax2.plot(t, latencys, color=color)
ax2.tick_params(axis='y', labelcolor=color)
fig.tight_layout()
plt.show()

```
