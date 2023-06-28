

Summary
=======


Trainning commands
------------------

```
python data/custom/prepare.py
```

```
python train.py config/train_custom.py --device=cuda --compile=False --eval_iters=20 --log_interval=1 --block_size=64 --batch_size=12 --n_layer=4 --n_head=4 --n_embd=128 --max_iters=2000 --lr_decay_iters=2000 --dropout=0.0
```

Generating inference commands
-----------------------------

```
python sample.py --out_dir=out-custom-char
```



Results
-------




| Block Size  | Iterations  | Time | Result |
|--- | --- | --- | --- |
| 64 | 2000 | 1:45 | [output 1](out/2kb64t4l5.txt) |
| 64 | 4000 | 3:24 | [output 2](out/4kb64t6m5l4.txt) |
| 64 | 10000 | 8:16 | [output 3](out/10kb64t1551l3.txt) |
| 64 | 40000 | 32:25    | [output 4](out/40kb64t32l26.txt) |

| Iterations  | Block Size  | Time | Result |
| --- | --- | --- | --- |
| 1000 | 64 | 8.16 | [output 5](out/10kb64t1551l3.txt) |
| 1000 | 128 | 14:20 | [output 6](out/10kb128t14l27.txt) |
| 1000 | 256 | 59:00 | [output 7](out/10kb256t59l17.txt) |









