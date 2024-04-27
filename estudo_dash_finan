import streamlit as st
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

def main():
    # Carregando os dados do arquivo
    file_path = r'C:\Users\Luiz Gomes\Desktop\Python 2.0\Base de dados Dashmodel\Prev x Real acumulado 2023.xlsx'
    df = pd.read_excel(file_path)

    # Criando uma página com o título
    st.title('Análise de Receitas e Despesas')

    # Filtrando apenas as colunas relevantes para o gráfico
    receitas_despesas = df[df.columns[2:6]]

    # Plotando o gráfico
    st.subheader('Gráfico de Comparação entre Previsto e Realizado - Receitas e Despesas')
    plt.figure(figsize=(10, 6))
    sns.barplot(data=receitas_despesas, ci=None)
    plt.title('Comparação entre Previsto e Realizado - Receitas e Despesas')
    plt.ylabel('Valor')
    plt.xticks(rotation=45, ha='right')
    plt.legend(title='Tipo', labels=['Previsto', 'Realizado'])
    plt.tight_layout()
    st.pyplot()

    # Exibindo a matriz detalhando os gastos
    st.subheader('Detalhamento dos Gastos')
    st.write(df)

if __name__ == "__main__":
    main()
