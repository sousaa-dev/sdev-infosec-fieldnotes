# Information Security Field Notes

Guia de segurança da informação e operações defensivas

Pablo Sousa Ribeiro | 2026 | Edição revisada

## 1. Fundamentos e objetivos

### Fundamentação teórica

A segurança da informação é uma disciplina de gestão e engenharia orientada à proteção de ativos e serviços. Confidencialidade limita o acesso a informações; integridade preserva sua correção; disponibilidade garante uso no momento necessário. Autenticidade identifica a origem de uma informação, enquanto rastreabilidade permite reconstruir decisões. Uma política eficaz relaciona cada controle a um objetivo de negócio.

### Estudo de caso

Considere um sistema de matrículas: divulgar dados pessoais é uma falha de confidencialidade; alterar notas indevidamente compromete integridade; interromper o registro de alunos durante inscrições afeta disponibilidade. Os controles precisam ser escolhidos conforme a consequência, não somente a tecnologia.

### Atividade aplicada

Classifique calendário público, notas, credenciais e backups. Para cada ativo, escreva proprietário, requisito de proteção e impacto de uma falha. Prefira um registro com justificativas a uma lista de ferramentas.

### Critérios de avaliação

A classificação deve explicar por que notas precisam de acesso restrito e por que o calendário exige disponibilidade e integridade.

## 2. Governança, riscos e conformidade

### Fundamentação teórica

Governança estabelece responsabilidade e direção; gestão de risco identifica cenários e seleciona tratamentos proporcionais. Uma política define obrigações; uma norma interna especifica requisitos; um procedimento descreve execução; uma evidência demonstra realização. Risco residual é o risco restante após controles e deve ser aceito pelo responsável competente.

### Estudo de caso

O risco de perda de documentos pode ser descrito como indisponibilidade de arquivos após falha de armazenamento. Impacto e probabilidade devem ter critérios definidos. Uma matriz ordinal de 1 a 5 permite priorização, mas o produto dos dois valores não representa uma probabilidade estatística.

### Atividade aplicada

Crie três riscos com ativo, cenário, impacto, probabilidade, controle, proprietário, prazo e evidência. Defina quais condições exigem escalonamento e revisão periódica.

### Critérios de avaliação

A aceitação de risco deve registrar premissas e responsável. Reduzir risco não implica eliminá-lo.

## 3. NIST CSF 2.0 e melhoria contínua

### Fundamentação teórica

O CSF 2.0 organiza objetivos em seis funções: Governar, Identificar, Proteger, Detectar, Responder e Recuperar. Elas se complementam e não representam uma sequência rígida. Um perfil atual registra resultados alcançados; o perfil desejado indica onde a organização pretende chegar. A análise de lacunas orienta investimento e responsabilidade.

### Estudo de caso

Uma organização com backups existentes e sem ensaio de recuperação pode ter evidência de proteção parcial, porém pouca evidência de recuperação. A lacuna orienta um teste controlado, não uma compra automática de software.

### Atividade aplicada

Mapeie cinco controles ao CSF, registre evidência atual e objetivo futuro. Elabore plano trimestral com prioridades, dependências, responsáveis e critérios de conclusão.

### Critérios de avaliação

O plano deve vincular cada melhoria a uma deficiência observável. Consulte a publicação original [1].

## 4. ISO 27001 e gestão de segurança

### Fundamentação teórica

A ISO/IEC 27001 descreve requisitos de um sistema de gestão de segurança da informação (SGSI). A ISO/IEC 27002 oferece orientações sobre controles. Um SGSI envolve escopo, liderança, avaliação de riscos, objetivos, operação, avaliação de desempenho e melhoria. A declaração de aplicabilidade documenta escolhas e justificativas relacionadas aos controles.

### Estudo de caso

Uma equipe precisa justificar por que um controle é aplicável a seus processos. O resultado não se resume a uma marca de conformidade: são necessários responsáveis, processos de revisão e evidências consistentes.

### Atividade aplicada

Proponha escopo de um SGSI fictício para um departamento de TI. Escreva objetivos mensuráveis, registro de riscos e procedimento de revisão de mudanças.

### Critérios de avaliação

Um estudo de referência não equivale a uma auditoria ou certificação. Consulte o catálogo oficial ISO [2].

## 5. Privacidade e minimização de dados

### Fundamentação teórica

Proteção de dados pessoais envolve propósito, necessidade, segurança e responsabilidade. O inventário deve identificar categorias de dados, finalidade, acesso, compartilhamento, retenção e descarte. No Brasil, a LGPD define obrigações e direitos; sua aplicação depende do contexto e da análise competente.

### Estudo de caso

Um relatório mensal de atendimento exige contagem de chamados e tempos médios. Incluir nomes e documentos pessoais desnecessários aumenta exposição sem melhorar o indicador.

### Atividade aplicada

Revise campos de uma planilha fictícia, classifique dados e proponha versão agregada. Indique responsável e regras de retenção em cada etapa.

### Critérios de avaliação

A proposta deve justificar campos mantidos e descartados. Consulte a Lei 13.709/2018 e a ANPD [3].

## 6. Redes, segmentação e confiança

### Fundamentação teórica

Redes conectam sistemas e transportam informações. Endereçamento IP, resolução DNS, transporte TCP/UDP e protocolos de aplicação cumprem funções distintas. Segmentação separa usuários, aplicações e dados conforme necessidades. O uso de conexões autenticadas e criptografadas complementa limites de rede.

### Estudo de caso

Um portal recebe solicitações de usuários; a aplicação consulta armazenamento privado. O desenho deve impedir acesso direto ao armazenamento por visitantes e limitar os fluxos ao necessário.

### Atividade aplicada

Desenhe usuário, interface, aplicação e dados. Registre origem, destino, finalidade e responsável por cada fluxo autorizado. Identifique pontos de coleta de registros.

### Critérios de avaliação

Cada fluxo precisa de uma justificativa operacional e controle de acesso; segmentação não substitui autorização da aplicação.

## 7. Criptografia e integridade

### Fundamentação teórica

Criptografia simétrica emprega uma chave compartilhada; criptografia assimétrica utiliza pares de chaves. Hashes produzem resumos de tamanho fixo, e assinaturas digitais oferecem verificação de origem e integridade sob condições de confiança. Criptografia não elimina a necessidade de autorização, gestão de chaves e recuperação.

### Estudo de caso

Para arquivar um relatório, a equipe usa proteção em repouso e acesso restrito. Um hash obtido de uma referência confiável permite comparar versões, mas não confirma que o documento seja seguro.

### Atividade aplicada

Crie matriz para confidencialidade, verificação de integridade e autenticidade. Para cada requisito, indique técnica adequada, procedimento de administração da chave e recuperação.

### Critérios de avaliação

Diferencie hash, criptografia e assinatura sem tratar os três como equivalentes.

## 8. Identidade, MFA e Zero Trust

### Fundamentação teórica

Autenticação confirma identidade; autorização decide acesso; auditoria registra ações. O acesso mínimo limita permissões ao trabalho necessário. MFA combina fatores independentes, enquanto a estratégia Zero Trust reavalia acesso com contexto e reduz confiança implícita.

### Estudo de caso

Um analista muda de departamento. Sua identidade permanece, mas as permissões anteriores devem ser revistas, e os novos direitos aprovados pelo proprietário dos dados.

### Atividade aplicada

Elabore uma matriz de papéis, fluxo de admissão, transferência e desligamento, e procedimento de acesso emergencial com revisão posterior.

### Critérios de avaliação

O acesso temporário deve expirar e a revogação deve ser verificável. Referência Microsoft [4].

## 9. Hardening e gestão de endpoints

### Fundamentação teórica

Uma baseline de configuração representa o estado esperado de um ativo. Controles incluem inventário, atualização, criptografia de dispositivo, administração restrita, proteção de endpoint e registros. A aplicação deve considerar dependências, disponibilidade e capacidade de retorno.

### Estudo de caso

Um servidor de relatórios necessita manutenção. A equipe verifica dependências, registra o estado atual, agenda janela, valida a aplicação e preserva recuperação autorizada.

### Atividade aplicada

Prepare checklist de revisão de Linux ou Windows: inventário, atualização, contas, serviços necessários, backups e registros. Especifique evidência de cada controle, sem modificar um sistema real.

### Critérios de avaliação

A ficha deve separar estado observado, requisito e ação sugerida; configurar sem validação pode afetar disponibilidade.

## 10. Microsoft 365 e proteção de identidades

### Fundamentação teórica

A proteção de um tenant envolve administração de identidades, dispositivos, aplicativos e dados. Microsoft Entra ID centraliza autenticação e controle de acesso; políticas de acesso condicional consideram sinais conforme licenciamento; ferramentas de gerenciamento de endpoints ajudam a aplicar configurações e atualizações.

### Estudo de caso

Uma empresa deseja proteger contas administrativas e dispositivos corporativos. O plano precisa prever contas de emergência aprovadas, acesso mínimo, teste controlado de políticas e revisão de experiências de usuários.

### Atividade aplicada

Desenvolva uma matriz com usuários administradores, usuários comuns, dispositivos e dados. Descreva objetivos, proprietários, validação e tratamento de exceções.

### Critérios de avaliação

Não confunda um relatório de configuração com garantia de proteção. Verifique licenciamento e documentação atual antes de implantação [4].

## 11. Monitoramento, SOC, SIEM e EDR

### Fundamentação teórica

Um SOC organiza pessoas e processos de monitoramento e resposta. SIEM consolida e correlaciona eventos; EDR fornece telemetria de endpoints e recursos de investigação. Logs devem ter contexto, horários consistentes, proteção de acesso e retenção adequada. Alertas exigem triagem e não comprovam incidentes isoladamente.

### Estudo de caso

Um erro de rotina de backup aparece junto de utilização elevada de disco. Registros ajudam a delimitar serviço, horário e dependências. A equipe valida contexto, identifica proprietário e acompanha correção.

### Atividade aplicada

Use dez registros fictícios com data UTC, componente, nível e descrição. Produza contagens e cronologia, priorize verificações de disponibilidade e documente hipóteses.

### Critérios de avaliação

O relatório distingue evento, alerta, incidente confirmado e ausência de evidência.

## 12. Gestão de vulnerabilidades e atualizações

### Fundamentação teórica

Gestão de vulnerabilidades combina inventário, análise de avisos de fornecedores, priorização por impacto e exposição, correção e verificação. Uma pontuação técnica é um insumo, não substituto do contexto de negócio. Mudanças necessitam aprovação e plano de manutenção.

### Estudo de caso

Uma biblioteca possui aviso de segurança. Identifique quais versões estão em uso por meio do inventário, leia orientação do fornecedor, avalie criticidade do serviço e planeje atualização.

### Atividade aplicada

Crie um quadro com componente, versão inventariada, aviso oficial, responsável, prioridade, prazo, mitigação autorizada e evidência posterior.

### Critérios de avaliação

A atividade deve avaliar documentação e versões, sem construir reproduções, explorar falhas ou testar alvos.

## 13. Resposta a incidentes e preservação de evidências

### Fundamentação teórica

Resposta envolve preparação, identificação, coordenação, recuperação e aprendizado. Preservar registros significa documentar origem, data, responsável e alterações autorizadas. Uma linha do tempo separa fatos, interpretações e lacunas. Decisões de contenção devem considerar impacto e autorização.

### Estudo de caso

Um serviço deixa de funcionar após manutenção. A equipe registra o chamado, consulta histórico de mudanças, estima impacto, aciona o proprietário e acompanha recuperação aprovada.

### Atividade aplicada

Escreva relatório com resumo, escopo, cronologia, evidências, decisões, comunicação, critérios de recuperação e ações posteriores. Use apenas dados fictícios.

### Critérios de avaliação

Uma conclusão deve apontar evidência e grau de certeza. Consulte orientação NIST [5].

## 14. Continuidade, recuperação e cópias

### Fundamentação teórica

RTO é a meta de tempo para recuperar um serviço; RPO representa perda de dados tolerável em termos temporais. Planos de backup precisam considerar dependências, integridade, proteção, acesso e ensaios de restauração. Ter uma cópia não prova que a recuperação funciona.

### Estudo de caso

Uma biblioteca digital aceita perder até 24 horas de alterações e precisa voltar em quatro horas. Determine prioridades de restauração e critérios de verificação de arquivos e aplicação.

### Atividade aplicada

Planeje restauração de documentos sintéticos em um local separado. Registre versão, tempo de recuperação, comparação com referência e resultado da validação.

### Critérios de avaliação

O plano deve permitir determinar se os objetivos foram atingidos sem alegar um ensaio que não aconteceu.

## 15. Desenvolvimento seguro e DevSecOps

### Fundamentação teórica

Segurança deve integrar requisitos, desenho, implementação e manutenção. Validação de entradas, autorização no servidor, bibliotecas atualizadas, revisão de mudanças e proteção de segredos são práticas essenciais. DevSecOps incorpora verificações adequadas ao ciclo de entrega.

### Estudo de caso

Uma aplicação recebe solicitações de edição de perfil. A autorização deve ser vinculada à identidade e ao recurso, independentemente dos dados enviados pela interface.

### Atividade aplicada

Defina requisitos de autorização, validação, classificação de dados e logging para uma aplicação fictícia. Crie critérios de aceitação e plano de revisão de dependências.

### Critérios de avaliação

A revisão deve identificar e corrigir condições de risco em código próprio, sem criar cargas de exploração.

## 16. IA, automação e governança

### Fundamentação teórica

Sistemas de IA e automações processam informações e podem tomar ações. Controle de acesso, minimização de dados, limites de ferramentas, revisão humana e registros são necessários para reduzir erros e ações indevidas. Conteúdo externo deve ser tratado como informação não confiável.

### Estudo de caso

Um chatbot interno resume chamados. Ele precisa acessar apenas campos autorizados, não transmitir dados sensíveis e não alterar configurações de infraestrutura autonomamente.

### Atividade aplicada

Modele um fluxo de resumo de chamados fictícios: entrada validada, minimização, processamento, revisão humana e saída. Especifique regras de retenção e acesso.

### Critérios de avaliação

O fluxo não deve incluir descoberta de alvos ou execução ofensiva. Decisões administrativas permanecem aprovadas por responsáveis.

## 17. Projeto integrador e indicadores

### Fundamentação teórica

Um programa de segurança relaciona controles a resultados mensuráveis. Indicadores precisam de denominador, período, fonte e proprietário. Percentual de ativos com revisão em dia, tempo de restauração observado e cobertura de registros são exemplos de métricas operacionais; não equivalem à ausência de riscos.

### Estudo de caso

Uma organização fictícia deseja revisar acesso, recuperar documentos e melhorar registros em 90 dias. Priorize com base em risco e dependências, registrando objetivos e responsabilidades.

### Atividade aplicada

Produza inventário, matriz de papéis, registro de riscos, diagrama de dados, critérios de instalação segura, plano de recuperação e indicadores. Apresente três prioridades à gestão.

### Critérios de avaliação

A avaliação deve demonstrar rastreabilidade entre risco, controle, evidência, responsável e prazo.

## Referências bibliográficas

- [1] NIST. The Cybersecurity Framework (CSF) 2.0. 2024. https://www.nist.gov/cyberframework
- [2] ISO. ISO/IEC 27001 - Information security management systems. https://www.iso.org/standard/27001
- [3] BRASIL. Lei nº 13.709, de 14 de agosto de 2018. https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
- [4] MICROSOFT. Zero Trust deployment with Microsoft 365. https://learn.microsoft.com/en-us/security/zero-trust/microsoft-365-zero-trust
- [5] NIST. Incident Response Recommendations and Considerations for Cybersecurity Risk Management. SP 800-61 Rev. 3. https://csrc.nist.gov/pubs/sp/800/61/r3/final
- [6] CISA. Cross-Sector Cybersecurity Performance Goals. https://www.cisa.gov/cross-sector-cybersecurity-performance-goals