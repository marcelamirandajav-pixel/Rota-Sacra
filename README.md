# Rota-Sacra
Guia para visitação ao Patrimônio Sacro

O objetivo do software é guiar usuários por rotas históricas da Igreja Católica, trazendo um breve resumo da arquitetura, história, obras de arte e o impacto cultural de cada ponto de parada. O software vai buscar igrejas históricas, capelas e monumentos católicos, funcionando não só como um buscador de trajeto para se chegar ao local, mas também com dados turístico-cultural, fotos, áudios, pequenos textos e informações diversas sobre visitação.

# Arquitetura e Escopo Técnico

1. Funcionalidades Principais (MVP)
•	Mapeamento e Geolocalização: Integração com mapas (Google Maps API ou Leaflet/OpenStreetMap) para traçar as rotas, mostrar os pontos de interesse (igrejas, mosteiros, monumentos) e calcular a distância/tempo técnico do percurso.
•	Guia Cultural Áudio/Visual: Cada ponto de parada exibe informações históricas, fotos da arquitetura e um player de áudio (como um audioguia de museu).
•	Passaporte Digital (Gamificação): Sempre que o usuário chegar fisicamente a uma igreja da rota (validado via GPS), ele ganha um "carimbo digital" em seu perfil, simulando o passaporte real de grandes caminhos de peregrinação.

2. Sugestão de Stack Tecnológica
•	Frontend (Interface): React Native ou Flutter (para aplicativo mobile) ou React/Vue.js (para plataforma Web responsiva).
•	Backend (Servidor): Node.js (Express), Python (FastAPI/Django) ou Java (Spring Boot) para gerenciar usuários, rotas e pontos históricos.
•	Banco de Dados: PostgreSQL com a extensão PostGIS ou MongoDB.

# Estrutura do Banco de Dados 

A estrutura do banco de dados a ser utilizado seguirá estas tabelas principais:
Tabela	Campos Principais	Objetivo
Usuário	id, nome, email, senha, data_cadastro	Cadastro de turistas/peregrinos.
Rota	id, nome, descricao, distancia_km, dificuldade	Dados gerais do caminho completo.
Ponto_Interesse	id, rota_id, nome, latitude, longitude, estilo_arquitetonico, historia	As igrejas, capelas ou monumentos da rota.
Visita_Checkin	id, usuario_id, ponto_id, data_visita	Registro de que o usuário esteve lá (para o passaporte digital).

# Plataforma de Execução:
Como o acesso poderá ser via aplicativo ou palataforma (acessado tanto pelo navegador do celular ou computador), JavaScript/TypeScript no front-end, aliado ao Python como linguagem de back-end.

# Recursos Nativos (Mapas e Áudio):
O software de rota turística precisará integrar APIs de mapas (como Google Maps API ou OpenStreetMap), geolocalização em tempo real e reprodutores de mídia (áudio e imagens).

