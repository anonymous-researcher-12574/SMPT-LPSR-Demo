SMPT: Spatial Masked Predictive Transformer (ECCV 2026 Submission #12574)

This repository serves as the official anonymous validation hub for SMPT,
providing real-world video evidence, industrial efficiency metrics, and
cross-domain generalization results.

📺 Real-World Operational Demonstration

The demonstration below showcases SMPT integrated into a live metropolitan
traffic monitoring system.

🎥 View the High-Altitude Demonstration Video

🛠️ Industrial Context & Edge Efficiency:

  - Altitude Variance: Operates at traffic nodes in altitude bands of 6m, 9m,
    and 12m, able to cope with severe distortion issues and drastic scale
    reductions (16 × 5 pixels source).
  - Hardware-Agnostic (CPU Breakthroughs):
      - Training: Performed on a top-of-the-line NVIDIA RTX 3090 GPU.
      - Inference (Deployment): Importantly, the video was recorded when
        deployed in real-time to a standard mid-range computer (Intel Core i5,
        no discrete GPU).
      - Effect: SMPT is very efficient for CPU-based systems, thus achieving a
        substantial increase in scale through current municipal office machines.
  - Scale of Deployment: Currently deployed at Stage 1 (40 high-traffic camera
    nodes) in a metropolitan city (>1 million people) deployment plan,
    targeting 200+ node deployments.

💰 Socio-Economic Impact

1.  There have been notable achievements from the application of SMPT from
    theoretical concept to the development of infrastructure within the
    metropolitan scale:
      - Cost Efficiency in Infrastructure (CAPEX): The use of the
        software-driven 10x Super-Resolution capability in SMPT allowed for the
        avoidance of replacing the entire hardware with 4K cameras. The cost
        savings amount to 5,000percamerasite**, totaling over **1,000,000 for
        the anticipated 200-node network.
2.  Increase in Operational Income: Through the improvement from the 31.4%
    accuracy rate of baselines to 82.5% Word Accuracy, there is an opportunity
    to increase the automation and efficiency of traffic monitoring and toll
    systems.
3.  Sustainability: By utilizing the ability to run SMPT models in real time
    using regular Core i5 processors, the power consumption and heat generation
    of high-end GPUs are minimized.

📊 Performance Benchmark (CCPD Dataset)

To prove generalization beyond synthetic data, we evaluated SMPT on the
large-scale CCPD (Real-world) benchmark:

| Model           | Category                 | PSNR (dB) ↑ | Char Acc ↑ | Word Acc ↑ |
| :-------------- | :----------------------- | :---------: | :--------: | :--------: |
| ESRGAN \[4\]    | Generic CNN              | 23.31       | 45.4%      | 0.9%       |
| TSRN \[8\]      | Text-Specific CNN        | 22.68       | 51.9%      | 1.2%       |
| SFT-GAN \[10\]  | Semantic CNN             | 22.76       | 52.8%      | 1.6%       |
| SwinIR \[5\]    | General Transformer      | 19.14       | 81.3%      | 31.4%      |
| **SMPT (Ours)** | **Proposed Transformer** | **23.18**   | **94.0%**  | **82.5%**  |

Discussion: Although ESRGAN has superior PSNR, it is unable to preserve semantic
identity. SMPT delivers an absolute gain of +51.1% compared to the best
performing baseline (SwinIR), clearly demonstrating the importance of
semantics-aware transformers for extreme restoration.

🌐 Future Horizon: Human & Textile Reconstruction

SMPT was designed as a domain agnostic semantic reconstructor. The following is
our ongoing scaling of SMPT architecture towards Virtual Try-On applications:

  - Task: Scaling up low resolution web-streamed "Try-on haul" videos from 360p
    to 1080p.
  - Data Scale: Training on proprietary data consisting of 500,000 frames of
    human-centric videos.
  - Goal: Texture and geometry reconstruction of non-rigid textiles and humans,
    where structural coherence plays an important role for e-commerce
    applications.

Disclamer: The following code repository is associated with an ECCV 2026
anonymous review process. To preserve double-blind reviewing principles, all
city names and authors' identities have been removed from this repository.
