# Mozilla CommonVoice

## Install deps
```
pip install librosa==0.8.1 matplotlib h5py 
```

## Prepare Dataset
```
cd egs/commonvoice

# Those stages are very time-consuming
bash prepare.sh --stage -1 --stop-stage 3
(actually this params don't seem to even work; didn't bother fixing it though; just manually set it at the top of the shell script.)

##  train
Cut statistics:
╒═══════════════════════════╤════════════╕
│ Cuts count:               │ 5122876    │
├─────────────────────────────────────────
│ Total duration (hh:mm:ss) │ 7598:10:45 │
├─────────────────────────────────────────
│ mean                      │ 5.3        │
├─────────────────────────────────────────
│ std                       │ 1.7        │
├─────────────────────────────────────────
│ min                       │ 0.1        │
├─────────────────────────────────────────
│ 25%                       │ 4.1        │
├─────────────────────────────────────────
│ 50%                       │ 5.2        │
├─────────────────────────────────────────
│ 75%                       │ 6.4        │
├─────────────────────────────────────────
│ 99%                       │ 9.7        │
├─────────────────────────────────────────
│ 99.5%                     │ 10.1       │
├─────────────────────────────────────────
│ 99.9%                     │ 10.5       │
├─────────────────────────────────────────
│ max                       │ 49.9       │
├─────────────────────────────────────────
│ Recordings available:     │ 5122876    │
├─────────────────────────────────────────
│ Features available:       │ 5122876    │
├─────────────────────────────────────────
│ Supervisions available:   │ 5122876    │
╘═══════════════════════════╧════════════╛
SUPERVISION custom fields:
Speech duration statistics:
╒══════════════════════════════╤════════════╤══════════════════════╕
│ Total speech duration        │ 7598:10:45 │ 100.00% of recording │
├───────────────────────────────────────────────────────────────────
│ Total speaking time duration │ 7598:10:45 │ 100.00% of recording │
├───────────────────────────────────────────────────────────────────
│ Total silence duration       │ 00:00:01   │ 0.00% of recording   │
╘══════════════════════════════╧════════════╧══════════════════════╛


##  dev
Cut statistics:
╒═══════════════════════════╤══════════╕
│ Cuts count:               │ 9600     │
├───────────────────────────┼──────────┤
│ Total duration (hh:mm:ss) │ 13:35:01 │
├───────────────────────────┼──────────┤
│ mean                      │ 5.1      │
├───────────────────────────┼──────────┤
│ std                       │ 1.8      │
├───────────────────────────┼──────────┤
│ min                       │ 1.3      │
├───────────────────────────┼──────────┤
│ 25%                       │ 3.7      │
├───────────────────────────┼──────────┤
│ 50%                       │ 4.9      │
├───────────────────────────┼──────────┤
│ 75%                       │ 6.3      │
├───────────────────────────┼──────────┤
│ 99%                       │ 9.9      │
├───────────────────────────┼──────────┤
│ 99.5%                     │ 10.1     │
├───────────────────────────┼──────────┤
│ 99.9%                     │ 10.5     │
├───────────────────────────┼──────────┤
│ max                       │ 11.0     │
├───────────────────────────┼──────────┤
│ Recordings available:     │ 9600     │
├───────────────────────────┼──────────┤
│ Features available:       │ 9600     │
├───────────────────────────┼──────────┤
│ Supervisions available:   │ 9600     │
╘═══════════════════════════╧══════════╛
SUPERVISION custom fields:
Speech duration statistics:
╒══════════════════════════════╤══════════╤══════════════════════╕
│ Total speech duration        │ 13:35:01 │ 100.00% of recording │
├──────────────────────────────┼──────────┼──────────────────────┤
│ Total speaking time duration │ 13:35:01 │ 100.00% of recording │
├──────────────────────────────┼──────────┼──────────────────────┤
│ Total silence duration       │ 00:00:01 │ 0.00% of recording   │
╘══════════════════════════════╧══════════╧══════════════════════╛


##  test
Cut statistics:
╒═══════════════════════════╤══════════╕
│ Cuts count:               │ 9600     │
├───────────────────────────┼──────────┤
│ Total duration (hh:mm:ss) │ 14:20:55 │
├───────────────────────────┼──────────┤
│ mean                      │ 5.4      │
├───────────────────────────┼──────────┤
│ std                       │ 1.9      │
├───────────────────────────┼──────────┤
│ min                       │ 1.0      │
├───────────────────────────┼──────────┤
│ 25%                       │ 3.9      │
├───────────────────────────┼──────────┤
│ 50%                       │ 5.1      │
├───────────────────────────┼──────────┤
│ 75%                       │ 6.7      │
├───────────────────────────┼──────────┤
│ 99%                       │ 10.2     │
├───────────────────────────┼──────────┤
│ 99.5%                     │ 10.4     │
├───────────────────────────┼──────────┤
│ 99.9%                     │ 10.9     │
├───────────────────────────┼──────────┤
│ max                       │ 21.7     │
├───────────────────────────┼──────────┤
│ Recordings available:     │ 9600     │
├───────────────────────────┼──────────┤
│ Features available:       │ 9600     │
├───────────────────────────┼──────────┤
│ Supervisions available:   │ 9600     │
╘═══════════════════════════╧══════════╛
SUPERVISION custom fields:
Speech duration statistics:
╒══════════════════════════════╤══════════╤══════════════════════╕
│ Total speech duration        │ 14:20:55 │ 100.00% of recording │
├──────────────────────────────┼──────────┼──────────────────────┤
│ Total speaking time duration │ 14:20:55 │ 100.00% of recording │
├──────────────────────────────┼──────────┼──────────────────────┤
│ Total silence duration       │ 00:00:01 │ 0.00% of recording   │
╘══════════════════════════════╧══════════╧══════════════════════╛
```

## Training & Inference
refer to [Training](../../README.md##Training&Inference)
