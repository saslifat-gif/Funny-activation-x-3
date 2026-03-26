# Funny-activation-x³

Inspired by Karpathy, I tried using x³ as the activation function 
in a neural network — mostly because I thought the loss curves would 
look interesting. And yes, they were.

Some runs produced straight lines (stuck), some exploded instantly, 
and some had a thick "bulky" section that looked like a man flexing 💪. 
That bulky part turned out to be the best runs — the network oscillating 
around the optimal solution before settling. I think this is what people 
call oscillation near convergence.

## Some charts — the bulky one is really good
![IMG_0804](https://github.com/user-attachments/assets/332ff938-9ab9-4e3f-a81e-2ab5171f95f9)
![IMG_0806](https://github.com/user-attachments/assets/ff602c11-5a49-43e1-905f-83e00ffccadc)
![IMG_0801](https://github.com/user-attachments/assets/886375fa-5319-48ce-a428-48e6902329cc)
![IMG_0794](https://github.com/user-attachments/assets/a32714b2-03e9-4b19-b05d-2d7e9454db09)


## Experiment Results

| Strategy | Success Rate |
|----------|-------------|
| Normalization only | 18/30 (60%) |
| Gradient clipping only | 0/30 (0%) |
| Both combined | 23/30 (77%) |

## Conclusion
The explosion happens in the forward pass, not the backward pass. 
Gradient clipping alone cannot save x³ networks with large inputs. 
Input normalization is essential.
