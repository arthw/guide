### Jupyter use conda env ###

1.
```
conda install nb_conda_kernels
```

2.
```
conda create -n my_env
conda activate my_env
conda install -c anaconda ipykernel

python -m venv my_env

python -m ipykernel install --user --name=my_env

jupyter-kernelspec uninstall venv
```

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
