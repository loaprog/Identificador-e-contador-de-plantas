# Identificador-e-contador-de-plantas
Este código em Python usa a biblioteca OpenCV para identificar e contar plantas em uma imagem, usando a cor verde como filtro para extrair as regiões de interesse

Requisito para utilizar:
- A "distância da amostra do solo" é uma medida da resolução de imagem do drone e é representada pelo GSD, que significa "Ground Sample Distance" em inglês. Com uma imagem capturada por um drone com uma resolução de 0,2 a 1,2 centímetros por pixel (GSD), é possível identificar e contar a quantidade de plantas em uma determinada área.

Logica aplicada:
A lógica do código começa lendo uma imagem e convertendo-a para o espaço de cores HSV. Em seguida, define um intervalo de cor verde e cria uma máscara binária para os pixels que se encontram dentro desse intervalo.

![image](https://user-images.githubusercontent.com/75463070/230780658-1c3b7ccf-5014-48bd-903d-00f1e3e37137.png)
![image](https://user-images.githubusercontent.com/75463070/230779927-57b00c9a-ae58-43b3-8ba0-beae9a4eb2de.png)
![image](https://user-images.githubusercontent.com/75463070/230779940-9701a988-987e-4885-a933-58f2534e2ac3.png)
![image](https://user-images.githubusercontent.com/75463070/230780695-9dcb5f2d-4344-4292-9d36-8aa0e070c3fe.png)


A imagem é então submetida a um filtro morfológico para remover ruídos e a função findContours() é usada para identificar os contornos das regiões verdes na imagem. Com os contornos identificados, é calculado o centro de cada planta e um círculo vermelho é desenhado em torno do centro.

![Identificador e contador](https://user-images.githubusercontent.com/75463070/230780012-0c32eb73-2528-4812-a70e-0e36828ee0ea.png)



