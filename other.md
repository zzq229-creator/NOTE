# tensorboard
```
from torch.utils.tensorboard import SummaryWriter

writer = SummaryWriter("logs")
for i in range(100):
    writer.add_scalar("y=2x", 2*i, i)
pass
```

terminal中
tensorboard --logdir="logs" --port=6001
