#include <stdio.h>

#define MAX_FUNCIONARIOS 100

typedef struct {
    int inscricao;
    char nome[50];
    int classe;
    int horas_normais;
    int horas_extras;
} Funcionario;

void lerDados(Funcionario funcionarios[], int *n) {
    printf("Digite o numero de funcionarios: ");
    scanf("%d", n);

    for (int i = 0; i < *n; i++) {
        printf("\nFuncionario %d:\n", i + 1);
        printf("Numero de inscricao: ");
        scanf("%d", &funcionarios[i].inscricao);
        printf("Nome: ");
        scanf(" %[^\n]", funcionarios[i].nome);  
        printf("Classe (1 ou 2): ");
        scanf("%d", &funcionarios[i].classe);
        printf("Horas normais(no mes): ");
        scanf("%d", &funcionarios[i].horas_normais);
        printf("Horas extras: ");
        scanf("%d", &funcionarios[i].horas_extras);
    }
}

void calcularESalario(Funcionario funcionarios[], int n, float salario_referencia) {
    for (int i = 0; i < n; i++) {
        float salario_base;
        if (funcionarios[i].classe == 1) {
            salario_base = salario_referencia * 1.3;
        } else {
            salario_base = salario_referencia * 1.9;
        }

        float salario_hora = salario_base / 160; 
        float salario_normais = funcionarios[i].horas_normais * salario_hora;
        float salario_extras = funcionarios[i].horas_extras * salario_hora * 1.3;
        float salario_bruto = salario_normais + salario_extras;
        float desconto_inss = salario_bruto * 0.11;
        float salario_liquido = salario_bruto - desconto_inss;

        printf("\n=============================\n");
        printf("NUMERO DE INSCRICAO: %d\tNOME: %s\n", funcionarios[i].inscricao, funcionarios[i].nome);
        printf("SALARIO HORAS NORMAIS: %.2f\n", salario_normais);
        printf("SALARIO HORAS EXTRAS: %.2f\n", salario_extras);
        printf("DEDUCAO INSS: %.2f\n", desconto_inss);
        printf("SALARIO LIQUIDO: %.2f\n", salario_liquido);
    }
}

int main() {
    Funcionario funcionarios[MAX_FUNCIONARIOS];
    int n;
    float salario_referencia;

    printf("Digite o salario de referencia: ");
    scanf("%f", &salario_referencia);

    lerDados(funcionarios, &n);
    calcularESalario(funcionarios, n, salario_referencia);

    return 0;
}
