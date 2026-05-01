<h1>🛡️ Projeto: Simulação de Ataque Brute Force com Medusa e Kali Linux</h1>

<p>
  Este projeto faz parte da formação em Cibersegurança da <b>Digital Innovation One (DIO)</b>. 
  O objetivo é realizar uma auditoria de segurança prática, simulando ataques de força bruta em um ambiente controlado para identificar vulnerabilidades e propor medidas de mitigação.
</p>

<h2>🚀 Tecnologias e Ferramentas Utilizadas</h2>
<ul>
  <li><b>Sistema Operacional:</b> Kali Linux (ou Kali NetHunter via Termux)</li>
  <li><b>Alvo:</b> Metasploitable 2 / DVWA (Damn Vulnerable Web Application)</li>
  <li><b>Ferramentas:</b> Medusa, Nmap, e Wordlists personalizadas</li>
  <li><b>Rede:</b> Configuração Host-Only para isolamento de segurança</li>
</ul>

<h2>🛠️ Metodologia</h2>

<h3>1. Varredura e Reconhecimento</h3>
<p>
  Utilizei o <b>Nmap</b> para mapear os serviços ativos no alvo e identificar vetores de entrada, como portas 21 (FTP) e 22 (SSH).
</p>
<pre>
nmap -sV [IP_DO_ALVO]
</pre>

<h3>2. Execução do Ataque de Força Bruta</h3>
<p>
  Com a ferramenta <b>Medusa</b>, realizei testes de autenticação automatizados. Foquei na simulação de um cenário real de tentativa de quebra de credenciais administrativas.
</p>
<pre>
medusa -h [IP_DO_ALVO] -u admin -P wordlists/common_passwords.txt -M ftp
</pre>

<h3>3. Análise de Resultados</h3>
<p>
  A ferramenta permite validar rapidamente se o serviço possui senhas fracas ou previsíveis, auxiliando na verificação de políticas de segurança de usuários.
</p>

<h2>🛡️ Estratégias de Mitigação</h2>
<table>
  <thead>
    <tr>
      <th>Vulnerabilidade Identificada</th>
      <th>Medida de Prevenção Recomendada</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Senhas Fracas/Padronizadas</td>
      <td>Implementação de política de senhas complexas e MFA.</td>
    </tr>
    <tr>
      <td>Exposição de Portas Críticas</td>
      <td>Uso de Firewall e fechamento de serviços não essenciais.</td>
    </tr>
    <tr>
      <td>Tentativas Ilimitadas de Login</td>
      <td>Configuração de <i>Fail2Ban</i> para bloqueio temporário de IP.</td>
    </tr>
  </tbody>
</table>

<h2>📚 Conclusão</h2>
<p>
  A prática reforça a importância da segurança em camadas e da configuração correta de serviços de rede para evitar invasões automatizadas.
</p>
<hr>
<p align="center">
  Projeto desenvolvido por <b>Giih Sousa</b> como parte da Formação de Cybersecurity da DIO.
</p>


  
</p>
