# projeto_rv_visiostruct
Projeto para a cadeira de Realidade Virtual (RV) da Universidade Federal de Pernambuco

## Instruções de Uso (Android)

O projeto requer o uso da Unity Engine na versão 6000.0.43f1 ou superior, além de uma conta no Google Cloud para o uso das APIs do Google. 

1. Entre no Google Cloud Console e ative as APIs "Map Tiles API", "ARCore API" e "Places API (New)".
2. Crie uma chave de API, que será utilizada na aplicação Unity para acessar as APIs do Google.
3. Abra o projeto na Unity e navegue por File > Build Profiles > Player Settings, isso abrirá a janela "Project Settings".
4. Navegue até o dropdown "XR Plugin Mangement", escolha a opção "ARCore Extensions", mude a opção "Android Authentication Strategy" para "API Key", e no campo "Android API Key" coloque a chave de API do Google Cloud.
5. Na hierarquia de objetos do editor da Unity, clique no objeto "AR Geospatial Creator Origin", localize no inspetor o script "AR Geospatial Creator Origin" e insira sua chave de API no campo "Google Map Tiles API Key" contido nele.
6. O projeto já possui um modelo 3D de um prédio, mas você pode adicionar um modelo 3D de sua escolha, e para fazê-lo funcionar no ambiente AR basta adicioná-lo na cena, e no inspetor adicionar o "AR Geospatial Creator Anchor" ao objeto.


## Adicionando um modelo 3D ao espaço

Para fixar um Objeto 3D a um espaço geográfico, é necessário inserir o objeto e as coordenadas de latitude e longitude no projeto Unity, para isso:

1. Navegue até o Google Maps, selecione o local de interesse e copie as informações de latitude e longitude.
2. Abra o projeto e selecione o objeto "AR Geospatial Creator Origin" na hierarquia. Localize no inspetor o script "AR Geospatial Creator Origin" e preencha as informações do local escolhido nos campos de Latitude e Longitude.
3. Adicione seu Objeto 3D na cena e selecione-o na hierarquia. No inspetor, adicione um componente do tipo "AR Geospatial Creator Anchor" e preencha as informações do local escolhido nos campos de Latitude e Longitude.
4. No editor da cena, ajuste a posição, rotação e proporção do seu objeto.
5. Compile o projeto, instale-o em seu celular Android e vá até o local onde o Objeto 3D foi posicionado. Para melhores resultados ou visualização em ambientes internos, há uma checkbox "Occlusion" que ativa ou desativa a oclusão, facilitando a visualização do objeto.


