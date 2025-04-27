#include <stdio.h>

int main() {
    float vendas[12][4]; 
    float totalMes[12] = {0};    
    float totalSemana[4] = {0};  
    float totalAno = 0;          

    printf("Digite os valores de vendas da loja (12 meses x 4 semanas):\n");
    for (int mes = 0; mes < 12; mes++) {
        printf("Mes %d:\n", mes + 1);
        for (int semana = 0; semana < 4; semana++) {
            printf("  Semana %d: ", semana + 1);
            scanf("%f", &vendas[mes][semana]);
        }
    }

    for (int mes = 0; mes < 12; mes++) {
        for (int semana = 0; semana < 4; semana++) {
            totalMes[mes] += vendas[mes][semana];       
            totalSemana[semana] += vendas[mes][semana]; 
            totalAno += vendas[mes][semana];            
        }
    }

    printf("\nTotal vendido em cada mes:\n");
    for (int mes = 0; mes < 12; mes++) {
        printf("Mes %d: %.2f\n", mes + 1, totalMes[mes]);
    }

    printf("\nTotal vendido em cada semana do mes ao longo do ano:\n");
    for (int semana = 0; semana < 4; semana++) {
        printf("Semana %d R$: %.2f\n", semana + 1, totalSemana[semana]);
    }

    printf("\nTotal vendido no ano R$: %.2f\n", totalAno);

    return 0;
}
