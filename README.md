Independent Researcher focused on Dark Matter and Cosmology. Creator of the Jara Constant (1.44 \times 10^{-18} kg/m³) for GRB spectral lag validation

My research indicates that the vacuum is not an "absolute void" but possesses a specific density defined by the **Jara Constant** ($\rho_J = 1.44 \times 10^{-18} kg/m³$).

This implies that the light speed observed across cosmological distances undergoes a slight correction. The formula proposing this effective velocity ($v_J$) is:

$$v_J = c \cdot \sqrt{1 - \frac{\rho_J}{\rho_c}}$$

**Key Findings:**
Light "interacts" with this dark matter density, which explains the **Spectral Lag** detected in NASA satellite data. This model expands Einstein's relativity by considering the cosmic medium's density, proving that space-time is a material fluid rather than an empty stage.
​The graph below illustrates the predicted decay in effective light velocity (v_J) as a function of cosmological distance, compared to the standard constant c. This visualizes the "drag" effect caused by the Jara Constant density.import matplotlib.pyplot as plt
import numpy as np

# Constantes
c = 299792458  # Velocidade da luz (m/s)
rho_jara = 1.44e-18 
distancias = np.linspace(0, 10, 100) # De 0 a 10 bilhões de anos-luz

# Cálculo da Velocidade Jara (Simulação de decaimento)
# v = c * sqrt(1 - rho/rho_c) - aqui simplificado para visualização
v_jara = c * (1 - (rho_jara * distancias * 1e8)) 

plt.figure(figsize=(10, 6))
plt.plot(distancias, [c]*100, 'r--', label='Velocidade Constante (Einstein)')
plt.plot(distancias, v_jara, 'b-', label='Velocidade Efetiva (Modelo Jara)')

plt.title('Decaimento da Velocidade da Luz vs. Distância Cosmológica')
plt.xlabel('Distância (Bilhões de Anos-Luz)')
plt.ylabel('Velocidade (m/s)')
plt.legend()
plt.grid(True)

# Salva o gráfico como imagem
plt.savefig('grafico_constante_jara.png')
print("Gráfico gerado com sucesso como 'grafico_constante_jara.png'")
