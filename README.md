# 🛡️ AI Breach Coach - Week 8 Business Bending

**AI Breach Coach** es un asesor de ciberseguridad para ciudadanos mexicanos que descubrieron que sus datos fueron robados o usados de forma maliciosa.

## ¿Qué hace?

1. **Clasificación de amenazas** — Procesa tu descripción y identifica el tipo de ataque (fraude, suplantación, phishing, etc.)
2. **Plan de acción inmediato** — Proporciona 5 pasos para HOY, esta semana, y próximas semanas
3. **Recursos México** — Links y teléfonos de Fiscalía, INAI, PROFECO, y asistencia legal gratuita
4. **Interfaz conversacional** — Chat simple en español, móvil-first, sin configuración complicada

## Problema

Andrea descubrió que alguien usó su video de TikTok para montar un fraude en GoFundMe. No sabía qué hacer:
- ¿Es un crimen?
- ¿Puedo ir a la policía?
- ¿Puedo recuperar el dinero que recaudaron?
- ¿Qué hago ahora?

195 millones de mexicanos en el leak del gobierno 2026 enfrentan el mismo vacío: **nadie les dice qué hacer.**

## Stack

- **Frontend:** React 18 + Tailwind CSS (mobile-first)
- **LLM:** Claude API (con fallback local)
- **Data:** JSON local con 5 tipos de amenazas + 80+ pasos de acción + 5 recursos México
- **Deployment:** Vercel (static site)
- **Auth:** Ninguna (MVP stateless)

## Uso Local

```bash
# Clonar
git clone <repo>
cd w08-breach-coach

# Abrir en navegador
python3 -m http.server 3000
# Luego: http://localhost:3000/src/index.html
```

## Deployment Vercel

1. Push a GitHub
2. En Vercel: Connect repository
3. Set environment variable: `REACT_APP_CLAUDE_KEY` = tu API key
4. Deploy

La app funciona incluso sin Claude API (usa base de datos local).

## Roadmap 3 años

Si esto funciona, se convierte en:
- App nativa (iOS/Android)
- Plataforma de triage de ciberseguridad para ciudadanos mexicanos
- De facto victim-notification system cuando Mexico pase leyes de cybersecurity (2029+)

## Security Floor

✅ No secrets en código
✅ No datos personales reales en demos
✅ Inputs validados
✅ Respuestas de IA etiquetadas como "no legal"
✅ Sin autenticación requerida (MVP)

---

**Disclaimer:** ⚠️ Asesoramiento de IA, no legal. Para emergencias: Fiscalía 088
