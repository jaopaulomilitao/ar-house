# Planta Baixa em Realidade Aumentada

Aplicação de Realidade Aumentada (AR) baseada em web que rastreia uma imagem no mundo físico e projeta um modelo 3D animado de uma planta baixa sobre ela.

## 1. Tecnologias
* **[A-Frame](https://aframe.io/):** Motor de renderização para a cena 3D.
* **[MindAR](https://hiukim.github.io/mind-ar-js-doc/):** Biblioteca de rastreamento de imagem (*Image Tracking*) ultraleve e de alta performance para a web.

## 2. Como Funciona
A câmera do dispositivo escaneia o ambiente em busca da imagem alvo previamente compilada (`targets.mind`). Assim que o padrão é reconhecido (`targetFound`), a aplicação instancia um modelo 3D otimizado no formato `.glb` e emite um sinal para disparar uma animação suave de escala (`easeInOutQuad`), fazendo a planta "surgir" da imagem.

## 3. Como Executar
1. Por questões de segurança do navegador (acesso à câmera), é obrigatório rodar a aplicação através de um servidor local seguro (`localhost`) ou conexão `HTTPS`.
2. Autorize o uso da câmera quando solicitado.
3. Aponte a câmera para a imagem alvo definida no projeto para visualizar o modelo arquitetônico em 3D.
