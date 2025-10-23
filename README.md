[PROYECTO CLUSTTER.txt](https://github.com/user-attachments/files/23107248/PROYECTO.CLUSTTER.txt)
import React from "react";
import { motion } from "framer-motion";

// Landing futurista interactiva para Cluster Ingeniería y Seguridad
// Colores predominantes: celeste, blanco, azul, lila
// Placeholder para video e imágenes, se reemplazan luego

const VIDEO_URL = "https://your-storage.example.com/hero.mp4";
const LOGO_URL = "https://your-storage.example.com/logo.svg";
const DOCUMENT_URL = "https://your-storage.example.com/catalogo.pdf";
const WHATSAPP_LINK = "https://wa.me/569XXXXXXXX";

export default function FuturisticLanding() {
  return (
    <div className="min-https://chatgpt.com/canvas/shared/68fa6c03cd4881919805b16e560fc57eh-screen bg-gradient-to-b from-black via-slate-900 to-gray-900 text-white antialiased">
      {/* HERO */}
      <header className="relative overflow-hidden">
        <video className="w-full h-[60vh] object-cover brightness-75" autoPlay muted playsInline loop src={VIDEO_URL} />
        <div className="absolute inset-0 flex items-center justify-center pointer-events-none">
          <div className="max-w-4xl text-center px-6">
            <img src={LOGO_URL} alt="Cluster Ingeniería y Seguridad" className="mx-auto w-48 mb-6 pointer-events-auto" />
            <motion.h1 initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ delay: 0.4 }} className="text-3xl md:text-5xl font-extrabold tracking-tight text-cyan-400">
              Protección inteligente contra incendios
            </motion.h1>
            <motion.p initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.8 }} className="mt-4 text-lg md:text-xl text-blue-300 max-w-2xl mx-auto">
              Sistemas automáticos y semiautomáticos, recarga de extintores, detección de gases y soluciones para movilidad eléctrica.
            </motion.p>
            <div className="mt-8 flex gap-4 justify-center">
              <a href={DOCUMENT_URL} target="_blank" rel="noreferrer" className="px-6 py-3 rounded-2xl bg-gradient-to-r from-cyan-400 via-blue-400 to-lilac-400 text-black font-semibold shadow-lg hover:scale-105 transition-transform">
                Ver catálogo
              </a>
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="px-6 py-3 rounded-2xl border border-cyan-400 hover:bg-white/10 transition-colors">
                Contactar
              </a>
            </div>
          </div>
        </div>
        <div className="absolute inset-0 bg-gradient-to-t from-black/30 via-transparent to-black/50" />
        <div className="absolute inset-0">
          {/* Aquí se pueden agregar animaciones de cables y luces con canvas o Lottie */}
        </div>
      </header>
      {/* SECCIONES DE SERVICIOS */}
      <main className="py-16 px-6">
        <section className="max-w-6xl mx-auto">
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {[
              { title: "Supresión automática", desc: "Sistemas integrados para detección y extinción automática en incendios industriales.", color: "from-cyan-400 to-blue-500" },
              { title: "Recarga & mantenimiento", desc: "Recarga de extintores, pruebas hidráulicas y planes de mantención.", color: "from-blue-400 to-lilac-400" },
              { title: "Detección de gases", desc: "Análisis de gases y detectores Altair — monitoreo continuo para ambientes críticos.", color: "from-cyan-300 to-cyan-500" }
            ].map((f, i) => (
              <motion.article key={i} initial={{ opacity: 0, y: 12 }} whileInView={{ opacity: 1, y: 0 }} transition={{ delay: 0.15 * i }} viewport={{ once: true }} className={bg-gradient-to-br ${f.color} p-6 rounded-3xl backdrop-blur-md border border-white/5 shadow-2xl hover:scale-105 transition-transform}>
                <div>
                  <h3 className="text-xl font-semibold text-white">{f.title}</h3>
                  <p className="mt-2 text-white/80">{f.desc}</p>
                </div>
              </motion.article>
            ))}
          </div>
        </section>
        {/* DEMO INTERACTIVA */}
        <section className="mt-16 max-w-6xl mx-auto text-center">
          <h2 className="text-2xl font-bold text-cyan-400">Demostración en tiempo real</h2>
          <p className="mt-3 text-blue-300 max-w-2xl mx-auto">Interactúa con nuestros servicios: descarga ficha técnica, solicita cotización o comunica incidencias.</p>
          <div className="mt-8 grid grid-cols-1 md:grid-cols-3 gap-6">
            <a href={DOCUMENT_URL} className="p-6 rounded-2xl border border-white/5 hover:scale-105 transition-transform bg-gradient-to-r from-cyan-400 to-blue-400">
              <div className="font-semibold text-white">Ficha técnica</div>
              <div className="mt-2 text-sm text-white/70">PDF descargable con especificaciones y normas.</div>
            </a>
            <a href={WHATSAPP_LINK} className="p-6 rounded-2xl border border-white/5 hover:scale-105 transition-transform bg-gradient-to-r from-blue-400 to-lilac-400">
              <div className="font-semibold text-white">Cotizar ahora</div>
              <div className="mt-2 text-sm text-white/70">Habla con nuestro equipo comercial.</div>
            </a>
            <button onClick={() => window.scrollTo({ top: 0, behavior: 'smooth' })} className="p-6 rounded-2xl border border-white/5 hover:scale-105 transition-transform bg-gradient-to-r from-cyan-300 to-blue-500">
              <div className="font-semibold text-white">Volver al inicio</div>
              <div className="mt-2 text-sm text-white/70">Regresa al video inicial.</div>
            </button>
          </div>
        </section>
        {/* Footer */}
        <footer className="mt-20 border-t border-white/5 pt-8 text-white/80">
          <div className="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
            <div>
              <img src={LOGO_URL} alt="logo" className="w-36 mb-2" />
              <div className="text-sm text-white/60">Cluster Ingeniería y Seguridad — Protección e innovación.</div>
            </div>
            <div className="flex gap-4 items-center">
              <a href={WHATSAPP_LINK} target="_blank" rel="noreferrer" className="px-4 py-2 rounded-lg border border-cyan-400 hover:bg-white/10">WhatsApp</a>
              <a href={DOCUMENT_URL} target="_blank" rel="noreferrer" className="px-4 py-2 rounded-lg border border-cyan-400 hover:bg-white/10">Descargar ficha</a>
            </div>
          </div>
        </footer>
        <style>{video { filter: saturate(1.2) contrast(1.05); }}</style>
      </main>
    </div>
  );
}







