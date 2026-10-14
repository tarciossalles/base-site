import React, { useState, useEffect } from 'react';
import { ChevronDown, ChevronUp, Menu, X, ArrowRight, ShieldCheck, Activity, Target, Smartphone, ChevronLeft, ChevronRight } from 'lucide-react';

// Tailwind is injected by the platform, but we'll use inline styles for strict color enforcement
// where utility classes might not perfectly match the specific requested hex codes if standard config isn't enough,
// though Tailwind's arbitrary values will work perfectly.
const colors = {
  blackDeep: '#111111',
  blackSec: '#191919',
  white: '#FFFFFF',
  whiteSoft: '#F5F3F0',
  gray: '#A6A6A6',
  wineInst: '#641F31',
  wineDark: '#451522',
};

const Navbar = ({ scrolled }) => {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <nav className={`fixed w-full z-50 transition-all duration-300 ${scrolled ? 'bg-[#111111]/90 backdrop-blur-md border-b border-[#191919] py-4' : 'bg-transparent py-6'}`}>
      <div className="max-w-7xl mx-auto px-6 md:px-12 flex justify-between items-center">
        <div className="flex items-center gap-2">
          {/* Logo Placeholder - Using Text for crispness in the absence of an SVG logo */}
          <span className="font-['Poppins'] font-bold text-2xl tracking-tighter text-[#FFFFFF]">
            BASE<span className="text-[#641F31]">.</span>
          </span>
        </div>

        {/* Desktop Nav */}
        <div className="hidden md:flex items-center gap-8 text-sm font-medium tracking-widest text-[#A6A6A6]">
          <a href="#metodo" className="hover:text-[#FFFFFF] transition-colors uppercase">Método</a>
          <a href="#experiencia" className="hover:text-[#FFFFFF] transition-colors uppercase">Experiência</a>
          <a href="#planos" className="hover:text-[#FFFFFF] transition-colors uppercase">Planos</a>
          <button className="bg-[#641F31] hover:bg-[#451522] text-[#FFFFFF] px-6 py-2 rounded-sm transition-colors uppercase tracking-wider text-xs font-bold">
            Começar Agora
          </button>
        </div>

        {/* Mobile Toggle */}
        <button className="md:hidden text-[#FFFFFF]" onClick={() => setIsOpen(!isOpen)}>
          {isOpen ? <X size={24} /> : <Menu size={24} />}
        </button>
      </div>

      {/* Mobile Menu */}
      {isOpen && (
        <div className="md:hidden absolute top-full left-0 w-full bg-[#111111] border-b border-[#191919] py-4 px-6 flex flex-col gap-4 shadow-2xl">
          <a href="#metodo" onClick={() => setIsOpen(false)} className="text-[#A6A6A6] text-sm uppercase tracking-widest">Método</a>
          <a href="#experiencia" onClick={() => setIsOpen(false)} className="text-[#A6A6A6] text-sm uppercase tracking-widest">Experiência</a>
          <a href="#planos" onClick={() => setIsOpen(false)} className="text-[#A6A6A6] text-sm uppercase tracking-widest">Planos</a>
          <button className="bg-[#641F31] text-[#FFFFFF] px-6 py-3 rounded-sm uppercase tracking-wider text-xs font-bold mt-2">
            Começar Agora
          </button>
        </div>
      )}
    </nav>
  );
};

const Hero = () => {
  return (
    <section className="relative min-h-screen flex items-center justify-center bg-[#111111] overflow-hidden pt-20">
      {/* Background elements for editorial depth */}
      <div className="absolute top-0 right-0 w-2/3 h-full opacity-20 pointer-events-none">
         {/* Placeholder for real editorial photo. Using a dark placeholder. */}
        <img 
          src="https://placehold.co/1200x1600/111111/451522?text=FOTOGRAFIA+EDITORIAL+ESPORTIVA" 
          alt="Atleta em ambiente escuro" 
          className="w-full h-full object-cover object-right"
        />
        <div className="absolute inset-0 bg-gradient-to-l from-transparent to-[#111111]"></div>
        <div className="absolute inset-0 bg-gradient-to-t from-[#111111] to-transparent"></div>
      </div>

      {/* Tactical Grid Overlay */}
      <div className="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGNpcmNsZSBjeD0iMSIgY3k9IjEiIHI9IjEiIGZpbGw9InJnYmEoMjU1LDI1NSwyNTUsMC4wNSkiLz48L3N2Zz4=')] opacity-50 pointer-events-none"></div>

      <div className="max-w-7xl mx-auto px-6 md:px-12 w-full relative z-10 grid md:grid-cols-12 gap-8 items-center">
        
        <div className="md:col-span-8 lg:col-span-7 flex flex-col justify-center">
          
          <div className="flex items-center gap-3 mb-6">
            <span className="w-8 h-[1px] bg-[#641F31]"></span>
            <span className="text-[#A6A6A6] text-xs font-bold tracking-[0.2em] uppercase font-['Share_Tech_Mono']">Método Elite</span>
          </div>

          <h1 className="font-['Poppins'] text-5xl md:text-6xl lg:text-7xl font-extrabold text-[#FFFFFF] leading-[1.05] tracking-tight mb-6">
            Uma rotina intensa exige estratégia.<br />
            <span className="text-transparent bg-clip-text bg-gradient-to-r from-[#FFFFFF] to-[#A6A6A6]">
              Nós criamos a estrutura que se adapta a você.
            </span>
          </h1>
          
          <p className="text-[#A6A6A6] text-lg md:text-xl font-['Poppins'] font-light max-w-2xl leading-relaxed mb-10">
            Esqueça os métodos que engessam o seu dia. Entregamos o planejamento tático, a previsibilidade e a flexibilidade necessárias para você alcançar a alta performance na vida real.
          </p>
          
          <div className="flex flex-col sm:flex-row gap-4 items-start sm:items-center">
            <button className="bg-[#FFFFFF] text-[#111111] hover:bg-[#F5F3F0] px-8 py-4 rounded-sm font-bold text-sm tracking-widest uppercase transition-all flex items-center gap-2 group w-full sm:w-auto justify-center">
              Conheça a Base
              <ArrowRight size={16} className="group-hover:translate-x-1 transition-transform" />
            </button>
            <a href="#metodo" className="text-[#FFFFFF] border border-[#333333] hover:border-[#A6A6A6] px-8 py-4 rounded-sm font-medium text-sm tracking-widest uppercase transition-all flex items-center justify-center w-full sm:w-auto">
              Como Funciona
            </a>
          </div>

          <div className="mt-16 pt-8 border-t border-[#191919] flex items-center justify-between opacity-60">
            <p className="text-xs text-[#A6A6A6] font-['Share_Tech_Mono'] tracking-widest">VER. 2026 // ALTA PERFORMANCE</p>
            <p className="text-xs text-[#A6A6A6] font-['Share_Tech_Mono'] tracking-widest">BASE — ELEVE O PADRÃO</p>
          </div>
        </div>
      </div>
    </section>
  );
};

const ProblemSection = () => {
  return (
    <section className="bg-[#F5F3F0] py-24 md:py-32 relative text-[#111111]">
      <div className="max-w-7xl mx-auto px-6 md:px-12 grid md:grid-cols-2 gap-16 items-center">
        <div>
          <h2 className="font-['Poppins'] text-4xl md:text-5xl font-bold leading-tight mb-8">
            A vida real não segue um planejamento perfeito.
          </h2>
          <div className="space-y-6 text-[#191919] font-['Poppins'] text-lg">
            <p>
              Reuniões de última hora, viagens não planejadas, responsabilidades familiares. A maioria dos métodos exige que sua vida pare para que eles funcionem.
            </p>
            <p>
              Quando o método exige perfeição, o resultado inevitável é a frustração. O problema não é a sua falta de foco, é a fragilidade do sistema que você está tentando seguir.
            </p>
          </div>
        </div>
        <div className="relative">
          <div className="aspect-square bg-[#111111] p-8 md:p-12 relative flex flex-col justify-end">
            {/* Tactical elements */}
            <div className="absolute top-4 right-4 text-[#A6A6A6] font-['Share_Tech_Mono'] text-xs">DIAGNÓSTICO 01</div>
            <div className="absolute bottom-4 right-4 w-4 h-4 border-r border-b border-[#641F31]"></div>
            <div className="absolute top-4 left-4 w-4 h-4 border-l border-t border-[#641F31]"></div>
            
            <h3 className="text-[#FFFFFF] font-['Poppins'] text-3xl font-bold mb-4">
              Menos improviso. Mais estrutura.
            </h3>
            <p className="text-[#A6A6A6] font-['Poppins']">
              Nossa proposta não é garantir que todos os dias serão fáceis. É construir uma base sólida o suficiente para suportar os dias em que nada dá certo.
            </p>
          </div>
        </div>
      </div>
    </section>
  );
};

const MethodSection = () => {
  const steps = [
    { num: '01', title: 'Diagnóstico', desc: 'Análise tática da sua rotina atual. Entendemos suas restrições, horários e pontos críticos antes de prescrever qualquer movimento.' },
    { num: '02', title: 'Missão', desc: 'Definição clara de objetivos reais. Sem metas irreais, apenas marcos progressivos e alcançáveis baseados no seu contexto.' },
    { num: '03', title: 'Execução', desc: 'Implementação do protocolo. Treinos otimizados, diretrizes claras e foco absoluto no que traz resultado com o menor desperdício de energia.' },
    { num: '04', title: 'Resultado', desc: 'Monitoramento contínuo. Ajustes finos na rota baseados em dados, garantindo que a consistência vença a motivação temporária.' }
  ];

  return (
    <section id="metodo" className="bg-[#111111] py-24 md:py-32 relative border-t border-[#191919]">
      <div className="max-w-7xl mx-auto px-6 md:px-12">
        <div className="mb-16">
          <h2 className="font-['Poppins'] text-4xl md:text-5xl font-bold text-[#FFFFFF] mb-4">
            Método <span className="text-[#641F31]">ELITE</span>
          </h2>
          <p className="text-[#A6A6A6] font-['Poppins'] text-lg max-w-2xl">
            Quatro fases de implementação tática. Um sistema desenvolvido para máxima eficiência, independente do cenário.
          </p>
        </div>

        <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8 relative">
          {/* Connector line for desktop */}
          <div className="hidden lg:block absolute top-12 left-0 w-full h-[1px] bg-[#191919] z-0"></div>

          {steps.map((step, index) => (
            <div key={index} className="relative z-10 flex flex-col">
              <div className="text-[#641F31] font-['Share_Tech_Mono'] text-5xl font-bold mb-6 bg-[#111111] inline-block pr-4">
                {step.num}
              </div>
              <h4 className="text-[#FFFFFF] font-['Poppins'] text-xl font-bold mb-4">{step.title}</h4>
              <p className="text-[#A6A6A6] font-['Poppins'] leading-relaxed text-sm">
                {step.desc}
              </p>
            </div>
          ))}
        </div>
      </div>
    </section>
  );
};

const PublicSection = () => {
  return (
    <section className="bg-[#191919] py-24 border-y border-[#333333]">
      <div className="max-w-7xl mx-auto px-6 md:px-12 grid md:grid-cols-2 gap-12 items-center">
        <div className="order-2 md:order-1 flex flex-col gap-4">
          
          {/* Perfil 1 */}
          <div className="flex gap-6 bg-[#111111] p-6 md:p-8 rounded-sm border border-[#333333] hover:border-[#641F31] transition-colors">
            <div className="text-[#641F31] font-['Share_Tech_Mono'] text-3xl font-bold leading-none">01</div>
            <div>
              <h3 className="text-[#FFFFFF] font-['Poppins'] font-bold tracking-wide mb-2 uppercase">Militares</h3>
              <p className="text-[#A6A6A6] text-sm leading-relaxed font-['Poppins']">
                Forças Armadas, tais como pilotos da Força Aérea Brasileira, Infantes, Intendentes, bem como Bombeiros e Policiais Militares que precisam conciliar preparação física, carreira e rotina operacional.
              </p>
            </div>
          </div>

          {/* Perfil 2 */}
          <div className="flex gap-6 bg-[#111111] p-6 md:p-8 rounded-sm border border-[#333333] hover:border-[#641F31] transition-colors">
            <div className="text-[#641F31] font-['Share_Tech_Mono'] text-3xl font-bold leading-none">02</div>
            <div>
              <h3 className="text-[#FFFFFF] font-['Poppins'] font-bold tracking-wide mb-2 uppercase text-sm sm:text-base">Profissionais de Alta Exigência</h3>
              <p className="text-[#A6A6A6] text-sm leading-relaxed font-['Poppins']">
                Pessoas com agendas intensas e que precisam de uma estratégia eficiente, tais como médicos, advogados e plantonistas. Pessoas que não têm tempo para improvisar.
              </p>
            </div>
          </div>

          {/* Perfil 3 */}
          <div className="flex gap-6 bg-[#111111] p-6 md:p-8 rounded-sm border border-[#333333] hover:border-[#641F31] transition-colors">
            <div className="text-[#641F31] font-['Share_Tech_Mono'] text-3xl font-bold leading-none">03</div>
            <div>
              <h3 className="text-[#FFFFFF] font-['Poppins'] font-bold tracking-wide mb-2 uppercase">Foco em Resultado</h3>
              <p className="text-[#A6A6A6] text-sm leading-relaxed font-['Poppins']">
                Pessoas que querem uma direção estratégica, dispostas a treinar e executar. Aqueles que aceitam o processo e buscam estruturação real para melhorar a estética e a saúde.
              </p>
            </div>
          </div>

        </div>
        <div className="order-1 md:order-2 lg:pl-12">
          <h2 className="font-['Poppins'] text-3xl md:text-4xl lg:text-5xl font-bold text-[#FFFFFF] mb-6 leading-tight">
            Para quem não tem o luxo do tempo livre.
          </h2>
          <p className="text-[#A6A6A6] font-['Poppins'] text-lg leading-relaxed">
            Se você tem controle total sobre suas 24 horas, qualquer método funciona. A BASE foi desenhada para a realidade: imprevisível, exigente e implacável.
          </p>
        </div>
      </div>
    </section>
  );
};

const DigitalExperience = () => {
  return (
    <section id="experiencia" className="bg-[#111111] py-24 md:py-32">
      <div className="max-w-7xl mx-auto px-6 md:px-12 grid md:grid-cols-12 gap-12 items-center">
        <div className="md:col-span-5">
          <div className="flex items-center gap-3 mb-6">
            <Smartphone className="text-[#641F31]" size={20} />
            <span className="text-[#A6A6A6] text-xs font-bold tracking-[0.2em] uppercase font-['Share_Tech_Mono']">Ecossistema Digital</span>
          </div>
          <h2 className="font-['Poppins'] text-4xl md:text-5xl font-bold text-[#FFFFFF] mb-6">
            Seu QG operacional.
          </h2>
          <p className="text-[#A6A6A6] font-['Poppins'] text-lg mb-8">
            Toda a sua estratégia consolidada em um único ambiente. Treinos, progressão de cargas, metas diárias e comunicação direta com a equipe. Sem planilhas confusas, sem aplicativos fragmentados.
          </p>
          <ul className="space-y-4">
            <li className="flex items-start gap-3">
              <div className="w-1.5 h-1.5 rounded-full bg-[#641F31] mt-2"></div>
              <p className="text-[#FFFFFF] text-sm font-medium font-['Poppins']">Acesso imediato ao planejamento da semana.</p>
            </li>
            <li className="flex items-start gap-3">
              <div className="w-1.5 h-1.5 rounded-full bg-[#641F31] mt-2"></div>
              <p className="text-[#FFFFFF] text-sm font-medium font-['Poppins']">Histórico de evolução e métricas de desempenho.</p>
            </li>
            <li className="flex items-start gap-3">
              <div className="w-1.5 h-1.5 rounded-full bg-[#641F31] mt-2"></div>
              <p className="text-[#FFFFFF] text-sm font-medium font-['Poppins']">Suporte tático integrado.</p>
            </li>
          </ul>
        </div>
        <div className="md:col-span-7 flex justify-center md:justify-end">
          {/* Smartphone Mockup */}
          <div className="relative w-[280px] sm:w-[300px] h-[600px] bg-[#000000] rounded-[2.5rem] border-[8px] border-[#191919] shadow-2xl overflow-hidden ring-1 ring-white/5">
            {/* Dynamic Island / Notch */}
            <div className="absolute top-0 inset-x-0 flex justify-center z-20 pointer-events-none">
              <div className="w-32 h-7 bg-[#191919] rounded-b-3xl"></div>
            </div>
            {/* Screen */}
            <img 
              src="IMG_8319.PNG" 
              alt="Interface do Aplicativo BASE" 
              className="absolute inset-0 w-full h-full object-cover object-top z-10"
            />
          </div>
        </div>
      </div>
    </section>
  );
};

const ResultsSection = () => {
  const [currentIndex, setCurrentIndex] = useState(0);

  // Aqui você pode adicionar seus 20 casos reais. 
  // Deixei 5 preenchidos como exemplo da estrutura.
  const results = [
    {
      id: "01",
      profile: "Plantonista / 34 anos",
      time: "6 Meses de Execução",
      description: "Redução de gordura corporal com manutenção de massa magra, mesmo com escalas de 24h consecutivas."
    },
    {
      id: "02",
      profile: "Militar / 28 anos",
      time: "8 Meses de Execução",
      description: "Aumento expressivo de força e condicionamento cardiovascular para testes de aptidão física."
    },
    {
      id: "03",
      profile: "Empresário / 41 anos",
      time: "12 Meses de Execução",
      description: "Reestruturação metabólica e ganho de massa consolidado, conciliando o método com viagens constantes e rotina imprevisível."
    },
    {
      id: "04",
      profile: "Advogada / 31 anos",
      time: "5 Meses de Execução",
      description: "Mudança estética radical e aumento de disposição, aplicando o método com precisão em intervalos curtos de tempo livre."
    },
    {
      id: "05",
      profile: "Piloto / 36 anos",
      time: "10 Meses de Execução",
      description: "Atingiu o ápice da performance física e prontidão operacional exigida pela corporação, sem depender de horários fixos."
    }
  ];

  const nextSlide = () => {
    setCurrentIndex((prev) => (prev === results.length - 1 ? 0 : prev + 1));
  };

  const prevSlide = () => {
    setCurrentIndex((prev) => (prev === 0 ? results.length - 1 : prev - 1));
  };

  return (
    <section className="bg-[#191919] py-24 md:py-32 border-t border-[#333333] overflow-hidden">
      <div className="max-w-7xl mx-auto px-6 md:px-12">
        <div className="mb-16 md:flex md:justify-between md:items-end">
          <div className="max-w-2xl">
            <div className="flex items-center gap-3 mb-4">
              <Target className="text-[#641F31]" size={20} />
              <span className="text-[#A6A6A6] text-xs font-bold tracking-[0.2em] uppercase font-['Share_Tech_Mono']">Evolução Tática</span>
            </div>
            <h2 className="font-['Poppins'] text-4xl md:text-5xl font-bold text-[#FFFFFF] mb-6">
              A execução se materializa no corpo.
            </h2>
            <p className="text-[#A6A6A6] font-['Poppins'] text-lg">
              Sem promessas mágicas ou edições. O que você vê aqui é o subproduto direto da aplicação disciplinada do Método ELITE na vida real.
            </p>
          </div>
          
          {/* Controles Desktop (Escondidos no mobile) */}
          <div className="hidden md:flex items-center gap-6 pb-2">
            <div className="text-[#A6A6A6] font-['Share_Tech_Mono'] tracking-widest text-sm">
              <span className="text-[#FFFFFF]">{String(currentIndex + 1).padStart(2, '0')}</span> // {String(results.length).padStart(2, '0')}
            </div>
            <div className="flex gap-2">
              <button onClick={prevSlide} className="w-12 h-12 flex items-center justify-center border border-[#333333] text-[#FFFFFF] hover:bg-[#641F31] hover:border-[#641F31] transition-all">
                <ChevronLeft size={20} />
              </button>
              <button onClick={nextSlide} className="w-12 h-12 flex items-center justify-center border border-[#333333] text-[#FFFFFF] hover:bg-[#641F31] hover:border-[#641F31] transition-all">
                <ChevronRight size={20} />
              </button>
            </div>
          </div>
        </div>

        {/* Carrossel */}
        <div className="relative">
          <div 
            className="flex transition-transform duration-500 ease-in-out"
            style={{ transform: `translateX(-${currentIndex * 100}%)` }}
          >
            {results.map((item, idx) => (
              <div key={idx} className="w-full flex-shrink-0 pr-0 md:pr-4">
                <div className="bg-[#111111] border border-[#333333] p-6 md:p-10 flex flex-col md:flex-row gap-8 md:gap-12 items-center group">
                  
                  {/* Imagens Antes/Depois */}
                  <div className="w-full md:w-1/2 grid grid-cols-2 gap-2">
                    {/* Imagem Antes */}
                    <div className="relative aspect-[4/5] bg-[#191919] overflow-hidden">
                      <div className="absolute top-3 left-3 z-10 bg-[#111111]/80 backdrop-blur-sm px-2 py-1 border border-[#333333]">
                        <span className="text-[#A6A6A6] text-[10px] font-bold tracking-widest uppercase font-['Share_Tech_Mono']">Antes</span>
                      </div>
                      {/* Substitua a URL abaixo pela foto de ANTES */}
                      <img 
                        src={`https://placehold.co/600x750/111111/333333?text=FOTO+ANTES+${item.id}`} 
                        alt={`Antes - Cliente ${item.id}`}
                        className="w-full h-full object-cover grayscale opacity-70 group-hover:opacity-100 group-hover:grayscale-0 transition-all duration-500"
                      />
                    </div>
                    {/* Imagem Depois */}
                    <div className="relative aspect-[4/5] bg-[#191919] overflow-hidden">
                      <div className="absolute top-3 right-3 z-10 bg-[#641F31]/90 backdrop-blur-sm px-2 py-1">
                        <span className="text-[#FFFFFF] text-[10px] font-bold tracking-widest uppercase font-['Share_Tech_Mono']">Depois</span>
                      </div>
                      {/* Substitua a URL abaixo pela foto de DEPOIS */}
                      <img 
                        src={`https://placehold.co/600x750/111111/641F31?text=FOTO+DEPOIS+${item.id}`} 
                        alt={`Depois - Cliente ${item.id}`}
                        className="w-full h-full object-cover grayscale opacity-90 group-hover:opacity-100 group-hover:grayscale-0 transition-all duration-500"
                      />
                    </div>
                  </div>

                  {/* Informações do Caso */}
                  <div className="w-full md:w-1/2 flex flex-col justify-center">
                    <div className="inline-block bg-[#191919] border border-[#333333] px-4 py-2 mb-6 w-fit">
                      <span className="text-[#A6A6A6] text-xs font-['Share_Tech_Mono'] tracking-widest uppercase">Relatório Operacional</span>
                    </div>
                    
                    <div className="flex items-center gap-4 mb-4">
                      <span className="text-[#641F31] font-['Share_Tech_Mono'] text-2xl font-bold">{item.id}</span>
                      <h3 className="text-[#FFFFFF] font-['Poppins'] text-xl md:text-2xl font-bold uppercase">{item.profile}</h3>
                    </div>
                    
                    <div className="text-[#FFFFFF] text-sm md:text-base font-['Share_Tech_Mono'] uppercase tracking-widest mb-6 pb-6 border-b border-[#333333]">
                      Duração do Ciclo: <span className="text-[#641F31] font-bold">{item.time}</span>
                    </div>
                    
                    <p className="text-[#A6A6A6] font-['Poppins'] text-base md:text-lg leading-relaxed">
                      "{item.description}"
                    </p>
                  </div>

                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Controles Mobile */}
        <div className="flex md:hidden items-center justify-between mt-8 border-t border-[#333333] pt-6">
          <div className="text-[#A6A6A6] font-['Share_Tech_Mono'] tracking-widest text-sm">
            <span className="text-[#FFFFFF]">{String(currentIndex + 1).padStart(2, '0')}</span> // {String(results.length).padStart(2, '0')}
          </div>
          <div className="flex gap-2">
            <button onClick={prevSlide} className="w-12 h-12 flex items-center justify-center bg-[#111111] border border-[#333333] text-[#FFFFFF] active:bg-[#641F31] transition-all">
              <ChevronLeft size={20} />
            </button>
            <button onClick={nextSlide} className="w-12 h-12 flex items-center justify-center bg-[#111111] border border-[#333333] text-[#FFFFFF] active:bg-[#641F31] transition-all">
              <ChevronRight size={20} />
            </button>
          </div>
        </div>

      </div>
    </section>
  );
};

const TestimonialsSection = () => {
  const testimonials = [
    {
      quote: "Sempre tentei me adaptar aos treinos de musculação genéricos, mas minha escala no hospital quebrava a sequência. A BASE não me deu uma planilha, me deu uma estratégia que funciona mesmo quando durmo mal ou viro a noite. O resultado estético veio como consequência da consistência que finalmente alcancei.",
      name: "Rodrigo M.",
      role: "Médico Cirurgião"
    },
    {
      quote: "Na aviação não temos margem para erro ou improviso. Eu precisava de um método de treinamento que refletisse essa mesma mentalidade tática. O acompanhamento, a análise de métricas no app e as avaliações constantes me deram a clareza exata de onde estou e para onde estou indo.",
      name: "Capitão Thiago C.",
      role: "Piloto da Força Aérea Brasileira"
    },
    {
      quote: "Eu não tinha tempo a perder com métodos que dependiam de um dia perfeito. O que me impressionou na BASE foi o Diagnóstico inicial. Eles entenderam minhas limitações de tempo e desenharam um plano executável. É disciplina aplicada de forma inteligente.",
      name: "Henrique F.",
      role: "Empresário do Setor Logístico"
    }
  ];

  return (
    <section className="bg-[#111111] py-24 md:py-32">
      <div className="max-w-7xl mx-auto px-6 md:px-12">
        <div className="text-center mb-16">
           <h2 className="font-['Poppins'] text-3xl md:text-4xl font-bold text-[#FFFFFF] mb-4">
            Feedback Operacional
          </h2>
          <p className="text-[#A6A6A6] font-['Poppins'] text-lg max-w-2xl mx-auto">
            A palavra de quem já abandonou as desculpas e executa o método na prática.
          </p>
        </div>

        <div className="grid md:grid-cols-3 gap-6 lg:gap-8">
          {testimonials.map((test, idx) => (
            <div key={idx} className="bg-[#191919] border border-[#333333] p-8 hover:border-[#641F31] transition-colors relative flex flex-col">
              {/* Aspas decorativas */}
              <div className="text-[#333333] text-6xl font-serif font-black absolute top-4 right-6 opacity-50 leading-none">
                "
              </div>
              <p className="text-[#A6A6A6] font-['Poppins'] text-sm leading-relaxed mb-8 relative z-10 flex-grow">
                {test.quote}
              </p>
              <div className="mt-auto border-t border-[#333333] pt-4 flex items-center gap-4">
                <div className="w-10 h-10 bg-[#333333] flex items-center justify-center font-['Share_Tech_Mono'] text-[#FFFFFF] font-bold text-sm">
                  {test.name.charAt(0)}
                </div>
                <div>
                  <h4 className="text-[#FFFFFF] font-['Poppins'] font-bold text-sm">{test.name}</h4>
                  <p className="text-[#641F31] font-['Share_Tech_Mono'] text-xs tracking-wider uppercase mt-1">{test.role}</p>
                </div>
              </div>
            </div>
          ))}
        </div>
      </div>
    </section>
  );
};

const PlansSection = () => {
  const plans = [
    {
      name: "Operação Starter",
      duration: "Trimestral",
      totalPrice: "750",
      installments: "3x R$ 250,00",
      desc: "Entrada no Método ELITE. Acesso ao nosso App com acompanhamento pelo ELITE Coach e Nutricionista.",
      features: [
        "Acesso completo ao App BASE",
        "Call de início com o ELITE Coach",
        "1 avaliação de feedback estratégico",
        "Sem suporte via WhatsApp"
      ],
      tag: "BASE//3 meses",
      highlight: false
    },
    {
      name: "Operação BASE",
      duration: "Semestral",
      totalPrice: "1.350",
      installments: "6x R$ 225,00",
      desc: "Construção e consolidação. Acompanhamento contínuo pelo ELITE Coach e Nutricionista para solidificar resultados.",
      features: [
        "Acesso completo ao App BASE",
        "Call com ELITE Coach e Nutricionista",
        "Suporte direto via WhatsApp",
        "3 avaliações periódicas de progresso"
      ],
      tag: "BASE//6 meses",
      highlight: true
    },
    {
      name: "Operação ELITE",
      duration: "Anual",
      totalPrice: "2.400",
      installments: "12x R$ 200,00",
      desc: "Jornada completa. Acesso total com acompanhamento estratégico de longo prazo pelo ELITE Coach e Nutricionista.",
      features: [
        "Acesso completo ao App BASE",
        "Call com ELITE Coach e Nutricionista",
        "Suporte VIP via WhatsApp",
        "4 avaliações periódicas de progresso"
      ],
      tag: "BASE//12 meses",
      highlight: false
    }
  ];

  return (
    <section id="planos" className="bg-[#111111] py-24 md:py-32 border-t border-[#191919]">
      <div className="max-w-7xl mx-auto px-6 md:px-12 text-center mb-16">
        <h2 className="font-['Poppins'] text-4xl md:text-5xl font-bold text-[#FFFFFF] mb-4">
          Assuma o Controle
        </h2>
        <p className="text-[#A6A6A6] font-['Poppins'] text-lg max-w-2xl mx-auto">
          Escolha o ciclo operacional adequado ao seu nível de comprometimento e exigência tática.
        </p>
      </div>

      <div className="max-w-7xl mx-auto px-6 lg:px-12 grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        {plans.map((plan, index) => (
          <div 
            key={index} 
            className={`flex flex-col relative p-8 transition-all duration-300 ${plan.highlight ? 'bg-[#191919] border-2 border-[#641F31] shadow-2xl transform lg:-translate-y-4' : 'bg-[#191919] border border-[#333333]'}`}
          >
            {plan.highlight && (
              <div className="absolute top-0 right-0 bg-[#641F31] text-[#FFFFFF] text-[10px] font-bold px-4 py-1.5 uppercase tracking-widest font-['Share_Tech_Mono']">
                Recomendado
              </div>
            )}
            
            <div className="mb-2">
              <span className="text-[#A6A6A6] text-xs font-bold tracking-[0.1em] uppercase font-['Share_Tech_Mono']">{plan.duration}</span>
            </div>
            
            <div className="mb-6">
              <h3 className="font-['Poppins'] text-2xl font-bold text-[#FFFFFF] mb-3">{plan.name}</h3>
              <p className="text-[#A6A6A6] text-sm font-['Poppins'] leading-relaxed min-h-[60px]">{plan.desc}</p>
            </div>
            
            <div className="mb-8 font-['Share_Tech_Mono'] pb-8 border-b border-[#333333]">
              <div className="flex items-baseline gap-1">
                <span className="text-[#A6A6A6] text-lg">R$</span>
                <span className="text-4xl font-bold text-[#FFFFFF]">{plan.totalPrice}</span>
              </div>
              <div className="text-[#641F31] text-sm mt-1">Ou {plan.installments} sem juros</div>
            </div>
            
            <ul className="space-y-5 mb-10 flex-grow font-['Poppins']">
              {plan.features.map((feature, idx) => (
                <li key={idx} className={`flex items-start gap-3 text-sm ${feature.includes('Sem suporte') ? 'text-[#666666]' : 'text-[#FFFFFF]'}`}>
                  <div className={`w-1.5 h-1.5 rounded-none mt-1.5 flex-shrink-0 ${feature.includes('Sem suporte') ? 'bg-[#333333]' : 'bg-[#641F31]'}`}></div> 
                  <span className="leading-snug">{feature}</span>
                </li>
              ))}
            </ul>

            <div className="mt-auto flex flex-col gap-4">
              <div className="text-right">
                 <span className="text-[#333333] text-xs font-['Share_Tech_Mono']">{plan.tag}</span>
              </div>
              <button className={`w-full py-4 font-bold uppercase tracking-widest text-xs transition-colors font-['Poppins'] ${plan.highlight ? 'bg-[#641F31] hover:bg-[#451522] text-[#FFFFFF]' : 'bg-[#FFFFFF] text-[#111111] hover:bg-[#F5F3F0]'}`}>
                Selecionar Operação
              </button>
            </div>
          </div>
        ))}
      </div>
    </section>
  );
};

const FAQItem = ({ question, answer }) => {
  const [isOpen, setIsOpen] = useState(false);
  return (
    <div className="border-b border-[#333333]">
      <button 
        className="w-full py-6 flex justify-between items-center text-left focus:outline-none"
        onClick={() => setIsOpen(!isOpen)}
      >
        <span className="font-['Poppins'] font-semibold text-[#FFFFFF] pr-4">{question}</span>
        {isOpen ? <ChevronUp className="text-[#A6A6A6] flex-shrink-0" /> : <ChevronDown className="text-[#A6A6A6] flex-shrink-0" />}
      </button>
      <div className={`overflow-hidden transition-all duration-300 ${isOpen ? 'max-h-96 pb-6' : 'max-h-0'}`}>
        <p className="text-[#A6A6A6] font-['Poppins'] text-sm leading-relaxed">{answer}</p>
      </div>
    </div>
  );
};

const FAQSection = () => {
  const faqs = [
    { 
      q: "O que é a BASE?", 
      a: "A BASE não é uma simples planilha de treinos. É uma estrutura completa baseada no Método ELITE, desenhada milimetricamente para pessoas que precisam conciliar alta performance física com uma rotina real, intensa e frequentemente imprevisível." 
    },
    { 
      q: "A BASE é uma consultoria online?", 
      a: "Nós oferecemos muito mais que um serviço de consultoria tradicional. Entregamos um ecossistema tático. Você não recebe apenas 'o que fazer' (treino e alimentação), mas sim uma estratégia executável para aplicar o Método ELITE e sustentá-lo dentro da sua realidade, sem depender de cenários perfeitos." 
    },
    { 
      q: "A BASE é exclusiva para militares?", 
      a: "Não. A BASE nasceu fortemente influenciada pela cultura de disciplina, preparação e prontidão do ambiente militar. Contudo, nossa estrutura foi arquitetada para qualquer profissional que viva uma rotina exigente e esteja disposto a abandonar desculpas para elevar seu padrão." 
    },
    { 
      q: "Preciso treinar em academia?", 
      a: "Sim. Para garantir a aplicação plena da nossa metodologia e os níveis de intensidade que exigimos, o acesso a uma infraestrutura de academia com equipamentos adequados é inegociável." 
    },
    { 
      q: "Como funciona depois que entro na BASE?", 
      a: "Iniciamos imediatamente com o Diagnóstico BASE: um mapeamento completo do seu cenário atual, restrições e objetivos. A partir disso, montamos sua estratégia no Método ELITE. Você recebe acesso ao nosso aplicativo próprio, onde executará os ciclos, receberá análises da equipe e terá a rota ajustada conforme avança." 
    },
    { 
      q: "O planejamento é personalizado?", 
      a: "Absolutamente. Nós não encaixamos você em um modelo pronto. O planejamento considera seu objetivo, condicionamento atual, rotina, disponibilidade de tempo e limitações. Construímos uma estratégia modular, compatível com a sua realidade e capacidade de execução." 
    },
    { 
      q: "Em quanto tempo terei resultados?", 
      a: "A BASE fornece a estrutura mais eficiente possível e a direção tática exata. Porém, a execução é sua. Não vendemos promessas mágicas de resultados em 30 dias porque trabalhamos com a realidade. Seu resultado e o tempo até ele serão diretamente proporcionais à sua disciplina e capacidade de manter a consistência dentro do nosso processo." 
    }
  ];

  return (
    <section className="bg-[#111111] py-24 md:py-32 border-t border-[#191919]">
      <div className="max-w-3xl mx-auto px-6 md:px-12">
        <h2 className="font-['Poppins'] text-3xl font-bold text-[#FFFFFF] mb-12 text-center">
          Dúvidas Frequentes
        </h2>
        <div>
          {faqs.map((faq, idx) => (
            <FAQItem key={idx} question={faq.q} answer={faq.a} />
          ))}
        </div>
      </div>
    </section>
  );
};

const Footer = () => {
  return (
    <>
      <section className="bg-[#0a0a0a] py-32 relative overflow-hidden border-t border-[#191919]">
        <div className="absolute inset-0 flex items-center justify-center opacity-5">
           <span className="text-[20vw] font-['Poppins'] font-black text-[#FFFFFF] tracking-tighter select-none">BASE</span>
        </div>
        <div className="max-w-4xl mx-auto px-6 text-center relative z-10">
          <h2 className="font-['Poppins'] text-5xl md:text-6xl font-bold text-[#FFFFFF] mb-8">
            Eleve o Padrão.
          </h2>
          <p className="text-[#A6A6A6] text-lg mb-12 font-['Poppins']">
            A decisão de abandonar a mediocridade é o primeiro passo. A estrutura para mantê-la é responsabilidade nossa.
          </p>
          <button className="bg-[#FFFFFF] text-[#111111] hover:bg-[#F5F3F0] px-10 py-5 rounded-sm font-bold text-sm tracking-widest uppercase transition-all shadow-xl hover:shadow-2xl font-['Poppins']">
            Iniciar Agora
          </button>
        </div>
      </section>

      <footer className="bg-[#111111] pt-16 pb-8 border-t border-[#191919]">
        <div className="max-w-7xl mx-auto px-6 md:px-12">
          <div className="flex flex-col md:flex-row justify-between items-center gap-8 mb-12">
            <img 
              src="white logo.png" 
              alt="BASE Logo" 
              className="h-14 w-auto object-contain mix-blend-screen"
            />
            <div className="flex gap-6 text-sm font-medium tracking-widest text-[#A6A6A6]">
              <a href="#" className="hover:text-[#FFFFFF] uppercase font-['Poppins']">Instagram</a>
              <a href="#" className="hover:text-[#FFFFFF] uppercase font-['Poppins']">Contato</a>
            </div>
          </div>
          <div className="flex flex-col md:flex-row justify-between items-center gap-4 text-xs text-[#666666] font-['Share_Tech_Mono'] border-t border-[#191919] pt-8">
            <p>© {new Date().getFullYear()} BASE. Todos os direitos reservados.</p>
            <div className="flex gap-4">
              <a href="#" className="hover:text-[#A6A6A6] font-['Poppins']">Termos de Uso</a>
              <a href="#" className="hover:text-[#A6A6A6] font-['Poppins']">Privacidade</a>
            </div>
          </div>
        </div>
      </footer>
    </>
  );
};

export default function App() {
  const [scrolled, setScrolled] = useState(false);

  useEffect(() => {
    const handleScroll = () => {
      setScrolled(window.scrollY > 50);
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  return (
    <div className="min-h-screen bg-[#111111] text-[#FFFFFF] selection:bg-[#641F31] selection:text-[#FFFFFF] font-['Poppins'] antialiased">
      {/* Injecting Fonts directly into the component for the preview environment */}
      <style dangerouslySetInnerHTML={{__html: `
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Share+Tech+Mono&display=swap');
      `}} />
      <Navbar scrolled={scrolled} />
      <main>
        <Hero />
        <ProblemSection />
        <MethodSection />
        <PublicSection />
        <DigitalExperience />
        <ResultsSection />
        <TestimonialsSection />
        <PlansSection />
        <FAQSection />
      </main>
      <Footer />
    </div>
  );
}
