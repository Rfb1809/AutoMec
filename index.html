<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AutoMec Pro - Gestão e Relatórios</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary: #2563eb;
            --primary-hover: #1d4ed8;
            --background: #f8fafc;
            --surface: #ffffff;
            --text: #1e293b;
            --text-secondary: #64748b;
            --border: #e2e8f0;
            --success: #16a34a;
            --warning: #eab308;
            --danger: #ef4444;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', system-ui, sans-serif; }
        body { background-color: var(--background); color: var(--text); padding: 20px; }
        .container { max-width: 1100px; margin: 0 auto; }
        
        header {
            text-align: center; margin-bottom: 30px; padding: 20px;
            background: var(--surface); border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }
        h1 { color: var(--primary); font-size: 26px; }

        .grid { display: grid; grid-template-columns: 1fr; gap: 20px; margin-bottom: 20px; }
        @media (min-width: 768px) { .grid { grid-template-columns: 1fr 1fr; } }

        .card {
            background: var(--surface); padding: 20px; border-radius: 8px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1); border: 1px solid var(--border);
        }
        h2 { font-size: 18px; margin-bottom: 15px; padding-bottom: 8px; border-bottom: 2px solid var(--border); }
        
        .form-group { margin-bottom: 12px; }
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        label { display: block; margin-bottom: 4px; font-weight: 600; font-size: 13px; }
        input, textarea {
            width: 100%; padding: 10px; border: 1px solid var(--border);
            border-radius: 6px; font-size: 14px; background: #fafafa;
        }
        input:focus, textarea:focus { outline: none; border-color: var(--primary); background: #fff; }
        
        button {
            width: 100%; padding: 11px; background-color: var(--primary); color: white;
            border: none; border-radius: 6px; font-size: 14px; font-weight: bold; cursor: pointer;
        }
        button:hover { background-color: var(--primary-hover); }
        .btn-dark { background-color: var(--text); }
        .btn-dark:hover { background-color: #0f172a; }

        /* Status de Alerta de Ligação */
        .status-badge {
            padding: 8px 12px; border-radius: 6px; font-weight: bold; font-size: 13px;
            margin-top: 10px; display: inline-block;
        }
        .status-ok { background-color: #dcfce7; color: var(--success); }
        .status-attention { background-color: #fef9c3; color: #a16207; }
        .status-alert { background-color: #fee2e2; color: var(--danger); }

        .result-box { margin-top: 15px; padding: 15px; background: #f1f5f9; border-radius: 6px; border-left: 4px solid var(--primary); }
        .maintenance-item { background: #fff; padding: 12px; margin-top: 10px; border-radius: 4px; border: 1px solid var(--border); }
        .price-tag { font-size: 12px; font-weight: bold; background: #e2e8f0; padding: 2px 6px; border-radius: 4px; }
        
        /* Área de Relatórios */
        .report-section { grid-column: 1 / -1; }
        .charts-container { display: grid; grid-template-columns: 1fr; gap: 20px; margin-top: 20px; }
        @media (min-width: 768px) { .charts-container { grid-template-columns: 1fr 1fr; } }
        .chart-box { max-height: 300px; position: relative; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>⚙️ AutoMec Pro</h1>
        <p style="color: var(--text-secondary); font-size: 14px;">Controle Financeiro, Histórico e Alertas de Retorno</p>
    </header>

    <div class="grid">
        <div class="card">
            <h2>Registrar Entrada / Serviço</h2>
            <form id="cadastroForm">
                <div class="form-row">
                    <div class="form-group">
                        <label>Placa:</label>
                        <input type="text" id="placa" required style="text-transform: uppercase;">
                    </div>
                    <div class="form-group">
                        <label>Modelo do Veículo:</label>
                        <input type="text" id="modelo" required>
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>Telefone do Cliente:</label>
                        <input type="text" id="telefone" placeholder="(00) 00000-0000" required>
                    </div>
                    <div class="form-group">
                        <label>Data do Serviço:</label>
                        <input type="date" id="dataServico" required>
                    </div>
                </div>
                <div class="form-group">
                    <label>Descrição dos Serviços:</label>
                    <textarea id="manutencao" placeholder="Ex: Troca de óleo 5w30 e filtro..." required></textarea>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>Valor Peças (R$):</label>
                        <input type="number" step="0.01" id="vPecas" value="0.00" required>
                    </div>
                    <div class="form-group">
                        <label>Mão de Obra (R$):</label>
                        <input type="number" step="0.01" id="vMaoObra" value="0.00" required>
                    </div>
                </div>
                <button type="submit">Salvar Ordem de Serviço</button>
            </form>
        </div>

        <div class="card">
            <h2>Consultar Placa & Próxima Troca</h2>
            <div class="form-row">
                <input type="text" id="buscaPlaca" placeholder="DIGITE A PLACA..." style="text-transform: uppercase;">
                <button type="button" class="btn-dark" id="btnBuscar">Buscar</button>
            </div>
            <div id="resultadoBusca" style="margin-top: 15px;">
                <p style="color: var(--text-secondary); text-align: center; font-style: italic;">Aguardando consulta...</p>
            </div>
        </div>

        <div class="card report-section">
            <h2>Relatórios Gerenciais e Gráficos</h2>
            <div class="form-row" style="align-items: flex-end;">
                <div class="form-group">
                    <label>Data Inicial:</label>
                    <input type="date" id="repDataInicio">
                </div>
                <div class="form-group">
                    <label>Data Final:</label>
                    <input type="date" id="repDataFim">
                </div>
                <div class="form-group" style="grid-column: span 2;">
                    <button type="button" class="btn-dark" id="btnGerarRelatorio">Gerar Relatório por Período</button>
                </div>
            </div>

            <div class="charts-container">
                <div class="chart-box">
                    <canvas id="chartFinancas"></canvas>
                </div>
                <div class="chart-box">
                    <canvas id="chartClientes"></canvas>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    // Inicialização do Banco local unificado
    if (!localStorage.getItem('oficina_pro_dados')) {
        localStorage.setItem('oficina_pro_dados', JSON.stringify([]));
    }

    // Define datas padrões nos inputs para facilitar
    document.getElementById('dataServico').valueAsDate = new Date();
    
    const hoje = new Date();
    const trintaDiasAtras = new Date();
    trintaDiasAtras.setDate(hoje.getDate() - 30);
    document.getElementById('repDataInicio').valueAsDate = trintaDiasAtras;
    document.getElementById('repDataFim').valueAsDate = hoje;

    // Salvar Dados
    document.getElementById('cadastroForm').addEventListener('submit', function(e) {
        e.preventDefault();

        const vPecas = parseFloat(document.getElementById('vPecas').value) || 0;
        const vMaoObra = parseFloat(document.getElementById('vMaoObra').value) || 0;

        const novaOS = {
            placa: document.getElementById('placa').value.trim().toUpperCase(),
            modelo: document.getElementById('modelo').value.trim(),
            telefone: document.getElementById('telefone').value.trim(),
            data: document.getElementById('dataServico').value,
            descricao: document.getElementById('manutencao').value.trim(),
            valorPecas: vPecas,
            valorMaoObra: vMaoObra,
            valorTotal: vPecas + vMaoObra
        };

        let banco = JSON.parse(localStorage.getItem('oficina_pro_dados'));
        banco.push(novaOS);
        localStorage.setItem('oficina_pro_dados', JSON.stringify(banco));

        alert('Ordem de serviço gravada com sucesso!');
        document.getElementById('cadastroForm').reset();
        document.getElementById('dataServico').valueAsDate = new Date();
        gerarGraficos();
    });

    // Buscar por Placa e Analisar Alerta de Ligação (Troca de Óleo - Base: 180 dias / 6 meses)
    document.getElementById('btnBuscar').addEventListener('click', function() {
        const placa = document.getElementById('buscaPlaca').value.trim().toUpperCase();
        if(!placa) return;

        const banco = JSON.parse(localStorage.getItem('oficina_pro_dados'));
        const historicoVeiculo = banco.filter(os => os.placa === placa).sort((a,b) => new Date(b.data) - new Date(a.data));

        if(historicoVeiculo.length === 0) {
            document.getElementById('resultadoBusca').innerHTML = `<p style="color:var(--danger)">Nenhum registro para a placa ${placa}.</p>`;
            return;
        }

        // Analisa a última manutenção realizada para ver o óleo
        const ultimaOS = historicoVeiculo[0];
        const dataUltima = new Date(ultimaOS.data + 'T00:00:00');
        
        // Calcula data ideal para próxima troca (180 dias depois)
        const dataProxima = new Date(dataUltima);
        dataProxima.setDate(dataUltima.getDate() + 180);
        
        const dataHoje = new Date();
        const diferencaDias = Math.ceil((dataProxima - dataHoje) / (1000 * 60 * 60 * 24));

        let htmlAlerta = '';
        if (diferencaDias < 0) {
            htmlAlerta = `<div class="status-badge status-alert">🚨 LIGAR AGORA! Passou ${Math.abs(diferencaDias)} dias do prazo de retorno.</div>`;
        } else if (diferencaDias <= 15) {
            htmlAlerta = `<div class="status-badge status-attention">⚠️ ATENÇÃO: Próxima troca em ${diferencaDias} dias. Ligue para agendar!</div>`;
        } else {
            htmlAlerta = `<div class="status-badge status-ok">✅ Em dia. Próxima revisão prevista para: ${dataProxima.toLocaleDateString('pt-BR')}.</div>`;
        }

        let htmlResult = `
            <div class="result-box">
                <h3>${ultimaOS.modelo} (${placa})</h3>
                <p><strong>Contato:</strong> ${ultimaOS.telefone}</p>
                ${htmlAlerta}
                <hr style="margin: 10px 0; border-color: var(--border);">
                <h4>Histórico de Atendimentos:</h4>
        `;

        historicoVeiculo.forEach(os => {
            const dataFmt = new Date(os.data + 'T00:00:00').toLocaleDateString('pt-BR');
            htmlResult += `
                <div class="maintenance-item">
                    <p><strong>Data:</strong> ${dataFmt}</p>
                    <p><strong>Serviço:</strong> ${os.descricao}</p>
                    <div style="margin-top:5px;">
                        <span class="price-tag">Peças: R$ ${os.valorPecas.toFixed(2)}</span>
                        <span class="price-tag">M.Obra: R$ ${os.valorMaoObra.toFixed(2)}</span>
                        <span class="price-tag" style="background:#bbf7d0">Total: R$ ${os.valorTotal.toFixed(2)}</span>
                    </div>
                </div>
            `;
        });

        htmlResult += `</div>`;
        document.getElementById('resultadoBusca').innerHTML = htmlResult;
    });

    // Variáveis globais para os objetos dos Gráficos (necessário para resetar ao filtrar)
    let chartFinancasInstance = null;
    let chartClientesInstance = null;

    function gerarGraficos() {
        const dataInicio = document.getElementById('repDataInicio').value;
        const dataFim = document.getElementById('repDataFim').value;

        const banco = JSON.parse(localStorage.getItem('oficina_pro_dados'));

        // Filtrar dados pelo período selecionado
        const dadosFiltrados = banco.filter(os => {
            return os.data >= dataInicio && os.data <= dataFim;
        }).sort((a,b) => new Date(a.data) - new Date(b.data));

        // Processar Dados Financeiros Totais
        let totalPecas = 0;
        let totalMaoObra = 0;
        
        // Processar Dados de Clientes por Dia
        let clientesPorDia = {};

        dadosFiltrados.forEach(os => {
            totalPecas += os.valorPecas;
            totalMaoObra += os.valorMaoObra;

            // Formata data para o gráfico de clientes
            const dataFmt = new Date(os.data + 'T00:00:00').toLocaleDateString('pt-BR', {day: 'numeric', month: 'short'});
            clientesPorDia[dataFmt] = (clientesPorDia[dataFmt] || 0) + 1;
        });

        // Destruir gráficos antigos se existirem para evitar sobreposição visual
        if(chartFinancasInstance) chartFinancasInstance.destroy();
        if(chartClientesInstance) chartClientesInstance.destroy();

        // 1. Gráfico Financeiro (Peças vs Mão de Obra)
        const ctxFin = document.getElementById('chartFinancas').getContext('2d');
        chartFinancasInstance = new Chart(ctxFin, {
            type: 'bar',
            data: {
                labels: ['Peças (R$)', 'Mão de Obra (R$)'],
                datasets: [{
                    label: 'Faturamento no Período',
                    data: [totalPecas, totalMaoObra],
                    backgroundColor: ['#3b82f6', '#10b981']
                }]
            },
            options: { responsive: true, maintainAspectRatio: false }
        });

        // 2. Gráfico Quantitativo de Clientes por Dia
        const ctxCli = document.getElementById('chartClientes').getContext('2d');
        chartClientesInstance = new Chart(ctxCli, {
            type: 'line',
            data: {
                labels: Object.keys(clientesPorDia),
                datasets: [{
                    label: 'Quantidade de Clientes / Veículos',
                    data: Object.values(clientesPorDia),
                    borderColor: '#ef4444',
                    backgroundColor: 'rgba(239, 68, 68, 0.1)',
                    fill: true,
                    tension: 0.2
                }]
            },
            options: { responsive: true, maintainAspectRatio: false }
        });
    }

    // Evento do botão de gerar relatório
    document.getElementById('btnGerarRelatorio').addEventListener('click', gerarGraficos);

    // Carrega os gráficos inicialmente ao abrir a tela
    window.onload = gerarGraficos;
</script>

</body>
</html>
