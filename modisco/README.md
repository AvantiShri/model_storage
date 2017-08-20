
`talgata_task0_positives_scores.npy` are scores generated from the deeplift
notebook at `https://github.com/kundajelab/deeplift/blob/2f26e03189262b321a2a764b806f5fb30145d51e/examples/public/genomics/genomics_simulation.ipynb` for talgata task 0,
using:
```
np.save("talgata_task0_positives_scores.npy",
        np.compress(condition=data.labels[:,0],
                    a=(method_to_task_to_scores['rescale_conv_revealcancel_fc_multiref_10'][0][:,None,:]*
                      onehot_data[:,0,:,:]).transpose(0,2,1),
                    axis=0))
```
Dimensions are 236 x 200 x 4
