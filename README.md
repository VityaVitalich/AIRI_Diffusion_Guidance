# AIRI_Diffusion_Guidance

Создание окружения: 

`conda env create -f env.yml`

`conda activate airi_env`

## Задачи по проекту

- [ ] Изучить теорию DDPM, classifier guidance, classifier-free guidance.   
> Для проверки того, понимаете ли вы как работает диффузия, нужно уметь отвечать на следующие вопросы
> 1. Как выглядит итерация обучения диффузионной модели
> 2. Как выглядит переход от x_t к x_{t-1} на этапе генерации
> 3. Как необходимо модифицировать итерацию генерации, чтобы получить classifier guidance
> 4. Как необходимо модифицировать итерацию генерации и модель, чтобы получить classifier-free guidance
- [ ] Разобраться в коде. Надо однозначно понимать, что происходит в файле 
[ddpm_sde.py](https://github.com/MeshchaninovViacheslav/AIRI_Diffusion_Guidance/blob/main/ddpm_sde.py), 
так как в нем описаны прямой и обратный процесс диффузии, 
и в файле [diffusion.py](https://github.com/MeshchaninovViacheslav/AIRI_Diffusion_Guidance/blob/main/diffusion.py), 
это основной класс для обучения модели.
- [ ] Дописать код обучения модели в функциях 
[calc_score](https://github.com/MeshchaninovViacheslav/AIRI_Diffusion_Guidance/blob/8cf7266866a5738fcb6bf2a9e40e6c33d61412a5/diffusion.py#L128),
[calc_loss](https://github.com/MeshchaninovViacheslav/AIRI_Diffusion_Guidance/blob/8cf7266866a5738fcb6bf2a9e40e6c33d61412a5/diffusion.py#L131C9-L131C18)
[sample_images](https://github.com/MeshchaninovViacheslav/AIRI_Diffusion_Guidance/blob/8cf7266866a5738fcb6bf2a9e40e6c33d61412a5/diffusion.py#L244).
Это задание преимущественно для Вити и Ильи. Так как это база, с которой дальше мы будем работать.
- 

## Материалы по проекту
1. Lil'Log https://lilianweng.github.io/posts/2021-07-11-diffusion-models/#conditioned-generation

### Список базовых статей
1. [DDPM](https://arxiv.org/pdf/2006.11239.pdf) 
2. [DDIM](https://arxiv.org/pdf/2010.02502.pdf)
3. [Improved DDPM](https://arxiv.org/pdf/2102.09672.pdf)
4. [Diffusion Models Beat GANs on Image Synthesis](https://arxiv.org/pdf/2105.05233.pdf)
5. [Score-based generative modeling through stochastic differential equations.](https://arxiv.org/pdf/2011.13456.pdf)
6. [Classifier-Free Diffusion Guidance](https://arxiv.org/pdf/2207.12598)
7. [Variational Diffusion Models](https://arxiv.org/pdf/2107.00630)

### Список статей для разбора
1. [Adding Conditional Control to Text-to-Image Diffusion Models](https://arxiv.org/pdf/2302.05543)
2. [Stay on topic with Classifier-Free Guidance](https://arxiv.org/pdf/2306.17806.pdf)
3. 