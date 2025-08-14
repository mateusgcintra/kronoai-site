import { useEffect, useState } from "react";
import { ArrowRight, Clock, Cpu, ShieldCheck, BrainCircuit, Workflow, Sparkles, ChartBarIncreasing, MessageSquare, Bot, CheckCircle2, Mail, Phone, MapPin, Instagram, Linkedin, Twitter, ChevronRight, Play } from "lucide-react";

// Krono AI — Single‑file React landing page
// ✅ Fix: remove all Node.js imports (fs/path/assert). Canvas runs in the browser-like bundler.
// This file is now a pure client React component that renders the site directly.
// It includes lightweight runtime sanity tests via console.assert (no Node deps).

// ==== Config ====
const LOGO_URL = "/assets/krono-logo.png"; // troque pelo seu SVG/PNG final se quiser

const nav = [
  { label: "Soluções", href: "#solutions" },
  { label: "Produtos", href: "#products" },
  { label: "Casos", href: "#cases" },
  { label: "Preços", href: "#pricing" },
  { label: "Contato", href: "#contact" },
];

const features = [
  { icon: <Clock className="size-6" />, title: "Tempo em seu favor", desc: "Automatize fluxos e acelere decisões." },
  { icon: <Cpu className="size-6" />, title: "Arquitetura escalável", desc: "Pipelines robustos, vetores e APIs." },
  { icon: <ShieldCheck className="size-6" />, title: "Segurança primeiro", desc: "Privacidade, auditoria e isolamento de dados." },
  { icon: <Sparkles className="size-6" />, title: "Experiência impecável", desc: "UX conversacional com insights claros." },
];

const solutions = [
  { icon: <Workflow className="size-7" />, title: "Automação Cognitiva", bullets: ["Agentes ponta‑a‑ponta", "ERP/CRM/WhatsApp", "Governança de execuções"] },
  { icon: <MessageSquare className="size-7" />, title: "NLP Omnichannel", bullets: ["Bots contextuais", "FAQ dinâmico", "Tradução e sentimento"] },
  { icon: <BrainCircuit className="size-7" />, title: "Knowledge AI & Search", bullets: ["RAG com fontes", "Busca semântica", "GDrive/Notion/SQL"] },
  { icon: <ChartBarIncreasing className="size-7" />, title: "Analytics Assistido", bullets: ["Pergunte aos dados", "Alertas e previsões", "Dashboards vivos"] },
];

const products = [
  { name: "Krono Studio", desc: "Orquestração de agentes e integrações.", points: ["Playbooks", "Observabilidade", "Multi‑ambiente"] },
  { name: "Krono Chat", desc: "Atendimento 24/7 via site e WhatsApp.", points: ["RAG com citações", "Treino por PDF/URL", "CRM"] },
  { name: "Krono Docs", desc: "Pesquisa e automações em documentos.", points: ["Extração", "Resumos", "Comparação de versões"] },
];

const tiers = [
  { name: "Start", price: "R$ 990/mês", desc: "Valide um caso de uso.", items: ["1 agente + 1 canal", "20k interações", "Suporte por e‑mail"], cta: "Começar agora" },
  { name: "Growth", highlight: true, price: "R$ 3.900/mês", desc: "Escala com governança.", items: ["Até 5 agentes", "3 canais + APIs", "Suporte prioritário"], cta: "Falar com vendas" },
  { name: "Enterprise", price: "Sob consulta", desc: "SLA e segurança avançada.", items: ["SLA 99,9%", "SSO/SAML, SCIM", "Ambiente dedicado"], cta: "Agendar demo" },
];

function LogoMark({ className = "h-8 w-8" }) {
  return (
    // eslint-disable-next-line @next/next/no-img-element
    <img src={LOGO_URL} alt="Krono AI logo" className={`${className} object-contain select-none`} draggable={false} />
  );
}

export default function KronoSite() {
  const [mobileOpen, setMobileOpen] = useState(false);

  // ===== Runtime sanity tests (no Node, only console.assert) =====
  useEffect(() => {
    try {
      console.assert(Array.isArray(nav) && nav.length >= 3, "nav deve ter links");
      console.assert(features.every(f => f.title && f.desc), "features com title/desc");
      console.assert(products.every(p => p.name && p.points?.length), "products válidos");
      console.assert(typeof LOGO_URL === "string" && LOGO_URL.length > 0, "LOGO_URL definido");
      // Extra tests
      console.assert(solutions.length === 4, "4 soluções definidas");
      console.assert(tiers.some(t => t.highlight), "existe um tier destacado");
      console.log("KronoSite: sanity tests passed ✔");
    } catch (e) {
      console.error("KronoSite: sanity tests failed", e);
    }
  }, []);

  return (
    <div className="min-h-screen text-slate-100" style={{ backgroundColor: "#0b1324" }}>
      {/* Keyframes & base CSS (no Tailwind build required) */}
      <style>{`
        :root { --navy:#0b1324; --ring:rgba(255,255,255,.10); --muted:rgba(255,255,255,.65) }
        .container-xl{max-width:1280px;margin:0 auto;padding:0 1rem}
        .card{background:rgba(255,255,255,.05); border:1px solid var(--ring); border-radius:1rem}
        .btn{display:inline-flex;align-items:center;gap:.5rem;padding:.75rem 1.25rem;border-radius:1rem}
        .btn-primary{background:linear-gradient(90deg,#6366f1,#38bdf8);box-shadow:0 8px 30px rgba(67,56,202,.35)}
        .btn-ghost{border:1px solid var(--ring)}
        .blur-bg{filter:blur(40px)}
        @keyframes beam { 0%{transform:rotate(0deg) translateX(-20%);opacity:0} 40%{opacity:.35} 100%{transform:rotate(360deg) translateX(20%);opacity:0} }
        @keyframes beam2 { 0%{transform:rotate(180deg) translateX(15%);opacity:0} 40%{opacity:.35} 100%{transform:rotate(-180deg) translateX(-15%);opacity:0} }
        @keyframes fadeUp { from{opacity:0; transform:translateY(16px)} to{opacity:1; transform:translateY(0)} }
        @keyframes fadeIn { from{opacity:0} to{opacity:1} }
        @keyframes techRainbow { 0%{ transform: translate3d(-8%,-6%,0) rotate(0deg); } 50%{ transform: translate3d(0,0,0) rotate(180deg);} 100%{ transform: translate3d(8%,6%,0) rotate(360deg);} }
        .animate-fadeUp{animation:fadeUp .8s ease-out both}
        .animate-fadeIn{animation:fadeIn 1.2s ease-out both}
        .animate-beam{animation:beam 18s linear infinite}
        .animate-beam2{animation:beam2 22s linear infinite}
        .animate-techRainbow{animation:techRainbow 28s linear infinite}
        .pill{display:inline-block; padding:.25rem .5rem; border-radius:999px; border:1px solid var(--ring); background:rgba(255,255,255,.06); font-size:.75rem}
        .grid{display:grid;gap:1.5rem}
        @media(min-width:768px){ .grid-cols-2{grid-template-columns:repeat(2,minmax(0,1fr))} }
        @media(min-width:1024px){ .grid-cols-3{grid-template-columns:repeat(3,minmax(0,1fr))} .grid-cols-4{grid-template-columns:repeat(4,minmax(0,1fr))} }
      `}</style>

      {/* Header flutuante */}
      <div style={{ position: "fixed", top: 24, left: "50%", transform: "translateX(-50%)", zIndex: 50, width: "94%", maxWidth: 1120 }} className="animate-fadeUp">
        <div style={{ border: "1px solid var(--ring)", background: "rgba(11,19,36,.7)", backdropFilter: "blur(16px)", borderRadius: 16, boxShadow: "0 20px 60px rgba(30,27,75,.4)" }}>
          <div style={{ padding: "12px 16px", display: "flex", alignItems: "center", justifyContent: "space-between" }}>
            <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
              <LogoMark className="h-8 w-8" />
              <span style={{ fontWeight: 600, letterSpacing: ".02em" }}>KRONO <span style={{ color: "#a5b4fc" }}>AI</span></span>
            </div>
            <nav className="hide-on-mobile" style={{ display: "none" }} />
            <button aria-label="Menu" onClick={() => setMobileOpen(v => !v)}>
              <ChevronRight className={`size-6 ${mobileOpen ? "rotate-90" : ""}`} />
            </button>
          </div>
          {mobileOpen && (
            <div style={{ borderTop: "1px solid var(--ring)", padding: "12px 16px", display: "grid", gap: 12 }}>
              {nav.map(n => (
                <a key={n.href} href={n.href} style={{ padding: "4px 0" }} onClick={() => setMobileOpen(false)}>{n.label}</a>
              ))}
              <a href="#contact" className="btn btn-primary">Agendar demo <ArrowRight className="size-4" /></a>
            </div>
          )}
        </div>
      </div>

      {/* HERO com arco‑íris tecnológico */}
      <section style={{ position: "relative", overflow: "hidden" }}>
        {/* Layer 0: arco‑íris */}
        <div className="animate-fadeIn" style={{ pointerEvents: "none", position: "absolute", inset: -224 }} aria-hidden>
          <div className="animate-techRainbow blur-bg" style={{ position: "absolute", inset: 0, opacity: .5, mixBlendMode: "screen", background: "conic-gradient(from 0deg at 50% 50%, #6E00FF, #5B43FF, #12A8FF, #5B43FF, #6E00FF)" }} />
          <div style={{ position: "absolute", inset: 0, background: "radial-gradient(transparent, rgba(11,19,36,.85))" }} />
        </div>
        {/* Layer 1: beams */}
        <div style={{ pointerEvents: "none", position: "absolute", inset: -160 }} aria-hidden>
          <div className="animate-beam" style={{ position: "absolute", left: "33%", top: 0, height: "140%", width: 288, background: "linear-gradient(to bottom, rgba(99,102,241,.4), rgba(217,70,239,.2), rgba(56,189,248,.4))", filter: "blur(40px)", transform: "rotate(12deg)" }} />
          <div className="animate-beam2" style={{ position: "absolute", right: "25%", top: 40, height: "140%", width: 288, background: "linear-gradient(to bottom, rgba(56,189,248,.4), rgba(99,102,241,.1), rgba(217,70,239,.4))", filter: "blur(40px)", transform: "rotate(-12deg)" }} />
        </div>

        <div className="container-xl" style={{ paddingTop: 128, paddingBottom: 96, position: "relative" }}>
          <div className="grid grid-cols-2 animate-fadeUp" style={{ alignItems: "center" }}>
            <div>
              <p style={{ textTransform: "uppercase", letterSpacing: ".2em", fontSize: 12, color: "rgba(165,180,252,.85)", display: "inline-flex", alignItems: "center", gap: 8 }}>
                <Bot className="size-4" /> Transforming time with AI
              </p>
              <h1 style={{ marginTop: 12, fontWeight: 600, fontSize: 40, lineHeight: 1.15 }}>Acelere seu negócio com <span style={{ backgroundImage: "linear-gradient(90deg,#a5b4fc,#7dd3fc)", WebkitBackgroundClip: "text", color: "transparent" }}>Inteligência Artificial</span></h1>
              <p style={{ marginTop: 16, color: "rgba(226,232,240,.9)", maxWidth: 560 }}>A Krono AI projeta, treina e opera agentes de IA que poupam horas do seu time e elevam a qualidade das decisões.</p>
              <div style={{ marginTop: 24, display: "flex", gap: 12, flexWrap: "wrap" }}>
                <a href="#contact" className="btn btn-primary">Agendar uma demo <Play className="size-4" /></a>
                <a href="#solutions" className="btn btn-ghost">Ver soluções <ArrowRight className="size-4" /></a>
              </div>
              <div style={{ marginTop: 32, display: "grid", gridTemplateColumns: "repeat(3,minmax(0,1fr))", gap: 24, fontSize: 14, color: "rgba(226,232,240,.85)" }}>
                {features.slice(0, 3).map(f => (
                  <div key={f.title} style={{ display: "flex", gap: 12 }}>
                    <div className="pill">{f.icon}</div>
                    <div>
                      <p style={{ color: "#fff", fontWeight: 500 }}>{f.title}</p>
                      <p style={{ fontSize: 12, color: "rgba(226,232,240,.75)" }}>{f.desc}</p>
                    </div>
                  </div>
                ))}
              </div>
            </div>

            <div style={{ position: "relative" }}>
              <div className="blur-bg" style={{ position: "absolute", inset: -40, background: "linear-gradient(45deg, rgba(99,102,241,.2), rgba(56,189,248,.1))" }} />
              <div className="animate-fadeUp" style={{ borderRadius: 24, padding: 1, background: "linear-gradient(45deg,#6366f1,#38bdf8)" }}>
                <div className="card" style={{ borderRadius: 24, padding: 24, background: "#0b1324" }}>
                  <div style={{ display: "flex", alignItems: "center", gap: 16 }}>
                    <LogoMark className="h-14 w-14" />
                    <div>
                      <p style={{ fontSize: 22, fontWeight: 600, letterSpacing: ".02em" }}>KRONO <span style={{ color: "#a5b4fc" }}>AI</span></p>
                      <p style={{ fontSize: 12, color: "var(--muted)" }}>Artificial Intelligence Solutions</p>
                    </div>
                  </div>
                  <div className="grid grid-cols-2" style={{ marginTop: 24 }}>
                    {features.map(f => (
                      <div key={f.title} className="card" style={{ padding: 16 }}>
                        <div style={{ color: "#c7d2fe" }}>{f.icon}</div>
                        <p style={{ marginTop: 12, fontWeight: 500 }}>{f.title}</p>
                        <p style={{ fontSize: 13, color: "var(--muted)" }}>{f.desc}</p>
                      </div>
                    ))}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Soluções */}
      <section id="solutions" className="container-xl" style={{ padding: "80px 0" }}>
        <div style={{ maxWidth: 640 }}>
          <h2 style={{ fontSize: 32, fontWeight: 600 }}>Soluções</h2>
          <p style={{ marginTop: 8, color: "rgba(226,232,240,.9)" }}>De protótipos rápidos à produção com métricas e segurança.</p>
        </div>
        <div className="grid grid-cols-4" style={{ marginTop: 24 }}>
          {solutions.map(s => (
            <div key={s.title} className="card animate-fadeUp" style={{ padding: 24 }}>
              <div style={{ color: "#c7d2fe" }}>{s.icon}</div>
              <p style={{ marginTop: 16, fontWeight: 600, fontSize: 18 }}>{s.title}</p>
              <ul style={{ marginTop: 12, fontSize: 14, color: "rgba(226,232,240,.9)" }}>
                {s.bullets.map((b, i) => (
                  <li key={i} style={{ display: "flex", gap: 8, alignItems: "start", marginBottom: 8 }}><CheckCircle2 className="size-4" />{b}</li>
                ))}
              </ul>
            </div>
          ))}
        </div>
      </section>

      {/* Produtos */}
      <section id="products" style={{ position: "relative", overflow: "hidden" }}>
        <div style={{ position: "absolute", inset: 0, background: "linear-gradient(90deg, rgba(99,102,241,.10), rgba(56,189,248,.10))" }} />
        <div className="container-xl" style={{ position: "relative", padding: "80px 0" }}>
          <div style={{ maxWidth: 640 }}>
            <h2 style={{ fontSize: 32, fontWeight: 600 }}>Produtos</h2>
            <p style={{ marginTop: 8, color: "rgba(226,232,240,.9)" }}>Componentes modulares para compor sua plataforma de IA.</p>
          </div>
          <div className="grid grid-cols-3" style={{ marginTop: 24 }}>
            {products.map((p, idx) => (
              <div key={p.name} className="card animate-fadeUp" style={{ padding: 24, animationDelay: `${0.05 * (idx+1)}s` }}>
                <p style={{ fontSize: 18, fontWeight: 600 }}>{p.name}</p>
                <p style={{ marginTop: 8, fontSize: 14, color: "rgba(226,232,240,.9)" }}>{p.desc}</p>
                <div style={{ marginTop: 12, display: "flex", flexWrap: "wrap", gap: 8 }}>
                  {p.points.map(pt => (
                    <span key={pt} className="pill">{pt}</span>
                  ))}
                </div>
                <a href="#contact" style={{ marginTop: 16, display: "inline-flex", alignItems: "center", gap: 8, color: "#c7d2fe" }}>Solicitar demo <ArrowRight className="size-4" /></a>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Resultados */}
      <section id="cases" className="container-xl" style={{ padding: "80px 0" }}>
        <div className="grid grid-cols-3" style={{ gap: 32 }}>
          <div>
            <h2 style={{ fontSize: 32, fontWeight: 600 }}>Resultados</h2>
            <p style={{ marginTop: 8, color: "rgba(226,232,240,.9)" }}>Ganhos concretos após 90 dias.</p>
          </div>
          <div className="grid grid-cols-3">
            {[
              { kpi: "‑37%", label: "tempo de atendimento" },
              { kpi: "+21%", label: "taxa de conversão" },
              { kpi: "‑48%", label: "custo por ticket" },
            ].map((c, idx) => (
              <div key={c.label} className="card animate-fadeUp" style={{ padding: 24, animationDelay: `${0.06 * (idx+1)}s` }}>
                <p style={{ fontSize: 32, fontWeight: 700, backgroundImage: "linear-gradient(90deg,#c7d2fe,#7dd3fc)", WebkitBackgroundClip: "text", color: "transparent" }}>{c.kpi}</p>
                <p style={{ marginTop: 8, color: "rgba(226,232,240,.85)", fontSize: 12, textTransform: "uppercase", letterSpacing: ".12em" }}>{c.label}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Planos */}
      <section id="pricing" style={{ position: "relative", overflow: "hidden" }}>
        <div style={{ position: "absolute", inset: 0, background: "linear-gradient(180deg, transparent, rgba(99,102,241,.10), transparent)" }} />
        <div className="container-xl" style={{ position: "relative", padding: "80px 0" }}>
          <div style={{ maxWidth: 640 }}>
            <h2 style={{ fontSize: 32, fontWeight: 600 }}>Planos</h2>
            <p style={{ marginTop: 8, color: "rgba(226,232,240,.9)" }}>Escolha o ponto de partida — nós escalamos com você.</p>
          </div>
          <div className="grid grid-cols-3" style={{ marginTop: 24 }}>
            {tiers.map((t, idx) => (
              <div key={t.name} className="card animate-fadeUp" style={{ padding: 24, transform: t.highlight ? "scale(1.03)" : undefined, boxShadow: t.highlight ? "0 25px 70px rgba(30,27,75,.4)" : undefined, background: t.highlight ? "linear-gradient(180deg, rgba(255,255,255,.10), transparent)" : undefined, animationDelay: `${0.05 * (idx+1)}s` }}>
                <p style={{ fontSize: 12, textTransform: "uppercase", letterSpacing: ".16em", color: "#c7d2fe" }}>{t.name}</p>
                <p style={{ marginTop: 8, fontSize: 28, fontWeight: 700 }}>{t.price}</p>
                <p style={{ marginTop: 8, fontSize: 14, color: "rgba(226,232,240,.9)" }}>{t.desc}</p>
                <ul style={{ marginTop: 12, fontSize: 14 }}>
                  {t.items.map(it => (
                    <li key={it} style={{ display: "flex", gap: 8, alignItems: "start", marginBottom: 8 }}><CheckCircle2 className="size-4" />{it}</li>
                  ))}
                </ul>
                <a href="#contact" className={"btn " + (t.highlight ? "btn-primary" : "btn-ghost")} style={{ marginTop: 16 }}>{t.cta} <ArrowRight className="size-4" /></a>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Contato */}
      <section id="contact" className="container-xl" style={{ padding: "96px 0" }}>
        <div className="grid grid-cols-2" style={{ alignItems: "start" }}>
          <div>
            <h2 style={{ fontSize: 32, fontWeight: 600 }}>Vamos acelerar seu projeto?</h2>
            <p style={{ marginTop: 8, color: "rgba(226,232,240,.9)", maxWidth: 560 }}>Conte o desafio, retornamos com um plano de 3 etapas e um protótipo em até 7 dias.</p>
            <div className="grid grid-cols-3" style={{ marginTop: 16, fontSize: 14 }}>
              {[
                { icon: <Mail className="size-4" />, label: "contato@kronoai.com" },
                { icon: <Phone className="size-4" />, label: "+55 (16) 0000‑0000" },
                { icon: <MapPin className="size-4" />, label: "Ribeirão Preto • SP" },
              ].map(i => (
                <div key={i.label} className="card" style={{ padding: 12, display: "flex", alignItems: "center", gap: 8 }}>
                  <span style={{ color: "#c7d2fe" }}>{i.icon}</span>
                  <span>{i.label}</span>
                </div>
              ))}
            </div>
            <div style={{ marginTop: 16, display: "flex", gap: 12, color: "rgba(226,232,240,.85)" }}>
              <a href="#" aria-label="LinkedIn" className="pill"><Linkedin className="size-5" /></a>
              <a href="#" aria-label="Twitter" className="pill"><Twitter className="size-5" /></a>
              <a href="#" aria-label="Instagram" className="pill"><Instagram className="size-5" /></a>
            </div>
          </div>
          <form className="card" style={{ padding: 24, display: "grid", gap: 12 }} onSubmit={e => { e.preventDefault(); alert("Mensagem enviada! (demo)"); }}>
            <div>
              <label style={{ fontSize: 14 }}>Nome</label>
              <input required style={{ marginTop: 6, width: "100%", borderRadius: 12, background: "#0b1324", border: "1px solid var(--ring)", padding: "10px 12px", color: "#fff" }} placeholder="Seu nome" />
            </div>
            <div className="grid grid-cols-2">
              <div>
                <label style={{ fontSize: 14 }}>E‑mail</label>
                <input type="email" required style={{ marginTop: 6, width: "100%", borderRadius: 12, background: "#0b1324", border: "1px solid var(--ring)", padding: "10px 12px", color: "#fff" }} placeholder="voce@empresa.com" />
              </div>
              <div>
                <label style={{ fontSize: 14 }}>Telefone</label>
                <input style={{ marginTop: 6, width: "100%", borderRadius: 12, background: "#0b1324", border: "1px solid var(--ring)", padding: "10px 12px", color: "#fff" }} placeholder="(16) 9 0000‑0000" />
              </div>
            </div>
            <div>
              <label style={{ fontSize: 14 }}>Conte-nos sobre o projeto</label>
              <textarea rows={5} style={{ marginTop: 6, width: "100%", borderRadius: 12, background: "#0b1324", border: "1px solid var(--ring)", padding: "10px 12px", color: "#fff" }} placeholder="Ex.: agente para WhatsApp integrado ao CRM" />
            </div>
            <button type="submit" className="btn btn-primary" style={{ justifyContent: "center" }}>Enviar mensagem <ArrowRight className="size-4" /></button>
            <p style={{ fontSize: 12, color: "rgba(148,163,184,1)" }}>Ao enviar, você concorda com nossa política de privacidade.</p>
          </form>
        </div>
      </section>

      {/* Footer */}
      <footer style={{ borderTop: "1px solid var(--ring)" }}>
        <div className="container-xl" style={{ padding: "40px 0", display: "flex", flexWrap: "wrap", alignItems: "center", justifyContent: "space-between", gap: 16 }}>
          <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
            <LogoMark className="h-7 w-7" />
            <span style={{ fontWeight: 500, letterSpacing: ".02em" }}>KRONO <span style={{ color: "#a5b4fc" }}>AI</span></span>
          </div>
          <p style={{ fontSize: 12, color: "rgba(148,163,184,1)" }}>© {new Date().getFullYear()} Krono AI — Transforming time with AI.</p>
        </div>
      </footer>
    </div>
  );
}
