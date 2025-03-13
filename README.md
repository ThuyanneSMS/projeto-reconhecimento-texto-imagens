# Projeto Prático: Reconhecimento de Texto em Imagens

Este projeto explora o uso de ferramentas de reconhecimento óptico de caracteres (OCR) para extrair texto de imagens. O objetivo é demonstrar como aplicar técnicas de processamento de imagens e inteligência artificial para resolver problemas do mundo real.

## 📂 Estrutura do Projeto

- **inputs/**: Contém as imagens utilizadas para o reconhecimento de texto.
- **output/**: Armazena os resultados do processamento (textos extraídos).
- **scripts/**: Contém os scripts usados para processar as imagens.

## 🛠️ Passo a Passo

1. **Preparação das Imagens**:
   - As imagens foram coletadas e salvas na pasta `inputs`.

2. **Processamento com OCR**:
   - Utilizei a biblioteca Tesseract (ou Azure OpenAI) para extrair texto das imagens.
   - Exemplo de código Python:
     ```python
     from PIL import Image
     import pytesseract

     # Caminho da imagem
     image_path = 'inputs/imagem1.png'

     # Extrair texto
     text = pytesseract.image_to_string(Image.open(image_path))
     print(text)

     # Salvar o resultado
     with open('output/resultado_imagem1.txt', 'w') as file:
         file.write(text)
     ```

3. **Resultados**:
   - Os textos extraídos foram salvos na pasta `output` como arquivos `.txt` ou `.json`.
  

## 📸 Prints do Processo

### Imagem Original
![Imagem Original](inputs/imagem1.png)

### Resultado Extraído

### Fluxo de Trabalho
![Fluxo de Trabalho](prints/fluxo.png)

## 💡 Insights e Aprendizados

- **Qualidade das Imagens**: Imagens com boa resolução e contraste geram resultados mais precisos.
- **Ferramentas de OCR**: Bibliotecas como Tesseract são gratuitas e eficientes, mas podem exigir ajustes para casos específicos.
- **Azure OpenAI**: Oferece recursos avançados de processamento de linguagem natural, mas requer configuração de API e pagamento conforme uso.

- ## 🚀 Possibilidades Futuras

- **Automação**: Criar uma interface gráfica ou API para facilitar o uso da ferramenta.
- **Integração com Outras Ferramentas**: Combinar OCR com tradução automática ou análise de sentimentos.
- **Escalabilidade**: Processar grandes volumes de imagens em paralelo usando serviços em nuvem.
