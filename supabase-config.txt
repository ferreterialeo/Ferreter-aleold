// Configuración de Supabase para Ferretería LD
// Esta clave es pública (publishable). Nunca pongas aquí una clave secret/service_role.

window.FERRETERIA_SUPABASE_URL = "https://uebkhzdwpfixvbaaewws.supabase.co";
window.FERRETERIA_SUPABASE_PUBLISHABLE_KEY = "sb_publishable_On0MN0DjzTTAOBiBvgICqQ_Kxp0B2rh";

// El cliente se crea cuando se carga la biblioteca oficial de Supabase.
if (window.supabase && typeof window.supabase.createClient === "function") {
  window.ferreteriaSupabase = window.supabase.createClient(
    window.FERRETERIA_SUPABASE_URL,
    window.FERRETERIA_SUPABASE_PUBLISHABLE_KEY
  );
} else {
  console.error(
    "Supabase no está cargado. Añade la biblioteca supabase-js antes de supabase-config.js."
  );
}
