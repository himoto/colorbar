# colorbar

## Vertical orientation

```python
import matplotlib.pyplot as plt
import matplotlib as mpl

plt.rcParams['font.size'] = 48
plt.rcParams['font.family'] = 'Arial'
plt.rcParams['axes.linewidth'] = 1

fig = plt.figure(figsize=(1, 9))
ax1 = fig.add_axes([0, 0, 1, 1])

cmap = mpl.cm.viridis
norm = mpl.colors.Normalize(vmin=0, vmax=12)

cb1 = mpl.colorbar.ColorbarBase(
    ax1, cmap=cmap,
    norm=norm,
    orientation='vertical'
)
cb1.set_label('colorbar')
cb1.set_ticks([0,3,6,9,12])
cb1.set_ticklabels([0,25,50,75,100])

plt.savefig(
    'colorbar_v.png',
    dpi=300,
    bbox_inches='tight'
)
```

## License
[MIT](/LICENSE)
