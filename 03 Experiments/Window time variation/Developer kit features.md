Performed evaluation of how the sliding window affects the performance of a RR model from 1-25 using the developer kit features

for all the regressions, I've used a dummy way to search a good alpha:
alphas = np.logspace(2, 7, num=10)

100 alpha to start is not hurting performance of the models with short window stimuli:
```
|   |   |   |
|---|---|---|
|67.5s|193|Stimulus Window: 1 \| Alpha: 0.01 -> Mean Accuracy: 0.17900000512599945|
|72.5s|194|Stimulus Window: 1 \| Alpha: 0.02636650898730358 -> Mean Accuracy: 0.17900000512599945|
|77.8s|195|Stimulus Window: 1 \| Alpha: 0.06951927961775606 -> Mean Accuracy: 0.17900000512599945|
|83.3s|196|Stimulus Window: 1 \| Alpha: 0.18329807108324356 -> Mean Accuracy: 0.17900000512599945|
|88.8s|197|Stimulus Window: 1 \| Alpha: 0.4832930238571752 -> Mean Accuracy: 0.17900000512599945|
|94.4s|198|Stimulus Window: 1 \| Alpha: 1.2742749857031335 -> Mean Accuracy: 0.17900000512599945|
|100.7s|199|Stimulus Window: 1 \| Alpha: 3.359818286283781 -> Mean Accuracy: 0.17900000512599945|
|107.2s|200|Stimulus Window: 1 \| Alpha: 8.858667904100823 -> Mean Accuracy: 0.17900000512599945|
|113.8s|201|Stimulus Window: 1 \| Alpha: 23.357214690901213 -> Mean Accuracy: 0.17900000512599945|
|120.4s|202|Stimulus Window: 1 \| Alpha: 61.584821106602604 -> Mean Accuracy: 0.17900000512599945|
|127.2s|203|Stimulus Window: 1 \| Alpha: 162.3776739188721 -> Mean Accuracy: 0.17900000512599945|
|134.2s|204|Stimulus Window: 1 \| Alpha: 428.13323987193957 -> Mean Accuracy: 0.17900000512599945|
|141.3s|205|Stimulus Window: 1 \| Alpha: 1128.8378916846884 -> Mean Accuracy: 0.17900000512599945|
|148.6s|206|Stimulus Window: 1 \| Alpha: 2976.3514416313133 -> Mean Accuracy: 0.17900000512599945|
|156.0s|207|Stimulus Window: 1 \| Alpha: 7847.5997035146065 -> Mean Accuracy: 0.17800000309944153|
|163.5s|208|Stimulus Window: 1 \| Alpha: 20691.3808111479 -> Mean Accuracy: 0.17800000309944153|
|171.0s|209|Stimulus Window: 1 \| Alpha: 54555.947811685146 -> Mean Accuracy: 0.17800000309944153|
|178.7s|210|Stimulus Window: 1 \| Alpha: 143844.988828766 -> Mean Accuracy: 0.1770000010728836|
|186.6s|211|Stimulus Window: 1 \| Alpha: 379269.01907322457 -> Mean Accuracy: 0.1770000010728836|
|194.4s|212|Stimulus Window: 1 \| Alpha: 1000000.0 -> Mean Accuracy: 0.17499999701976776|
```

## Full dataset

This experiment is using all the data expect the friends s6 to train and it's validation on the friends s6.
![[Pasted image 20250301094405.png]]



## Small subset