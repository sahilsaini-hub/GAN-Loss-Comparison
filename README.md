# GAN-Loss-Comparison
Models Evaluated: BCE GAN | LS-GAN | WGAN
Dataset: CIFAR-10
Training Duration: 50 Epochs

# 1. Key Observations

# WGAN (Wasserstein Loss)
Critic Loss: Fluctuates between -100 to 40

Generator Loss: Stabilizes near -40

Behavior:

Negative critic loss indicates the critic distinguishes real/fake effectively

Generator learns to "fool" the critic by maximizing its output (negative loss)

Characteristic of Wasserstein loss stability


![WGAN (Wasserstein Loss)](https://github.com/user-attachments/assets/5f1e3280-a3ce-4599-9e1e-df379abaee12)

# LS-GAN (Least Squares Loss)
Discriminator Loss: Decreases from 40 → 5

Generator Loss: Decreases from 35 → 15

Behavior:

Smooth convergence for both networks

Stable gradients from least squares loss prevent mode collapse


![LS](https://github.com/user-attachments/assets/3fdde85e-0421-4fbd-a766-ca965dc7d37f)

# BCE GAN (Binary Cross-Entropy)
Discriminator Loss: Oscillates 1.0 – 428.5

Generator Loss: Unstable (no clear trend)

Behavior:

Classic GAN instability (vanishing gradients)

Discriminator dominates training early

Generator struggles to catch up

![BCE](https://github.com/user-attachments/assets/4aeed76a-1f60-41dc-9bce-8206198dee24)

# Key Points to Highlight:

WGAN’s negative losses are normal (Wasserstein scores, not probabilities)

LS-GAN’s smooth training aligns with theoretical advantages

BCE GAN’s instability reflects classic GAN challenges

# Conclusion

Best Performer: LS-GAN (stable training, clear convergence)

Research Favorite: WGAN (theoretically grounded)

Legacy Approach: BCE GAN (baseline for comparison)

# Results align with GAN theory: LS-GAN’s least squares loss provides stable training, while WGAN’s Wasserstein metric enables meaningful loss interpretation. BCE GAN highlights classic adversarial training challenges
