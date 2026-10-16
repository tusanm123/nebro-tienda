
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#111827">
  <meta name="description" content="NEBRO México. Cargadores, cables, audífonos y baterías. Pide tus productos por WhatsApp.">
  <title>NEBRO México | Accesorios tecnológicos</title>

  <style>
    :root {
      --fondo: #f5f7fa;
      --texto: #172033;
      --oscuro: #111827;
      --acento: #087f8c;
      --verde: #20bd65;
      --blanco: #ffffff;
      --borde: #e5e7eb;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      color: var(--texto);
      background: var(--fondo);
    }

    a { color: inherit; }

    button, input { font: inherit; }

    button { cursor: pointer; }

    .barra {
      position: sticky;
      top: 0;
      z-index: 20;
      background: var(--oscuro);
      color: white;
      box-shadow: 0 3px 12px #0002;
    }

    .nav {
      max-width: 1150px;
      min-height: 70px;
      margin: auto;
      padding: 12px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
    }

    .logo {
      font-size: 27px;
      font-weight: 900;
      letter-spacing: 3px;
      color: white;
      text-decoration: none;
    }

    .logo span { color: #49d6d0; }

    .enlaces {
      display: flex;
      align-items: center;
      gap: 24px;
    }

    .enlaces a {
      text-decoration: none;
      font-size: 14px;
      font-weight: bold;
    }

    .enlaces a:hover { color: #49d6d0; }

    .hamburguesa {
      display: none;
      color: white;
      border: 1px solid #ffffff55;
      border-radius: 8px;
      padding: 8px 12px;
      background: transparent;
      font-size: 22px;
    }

    .hero {
      color: white;
      text-align: center;
      padding: 72px 20px;
      background:
        radial-gradient(ellipse at top right, #087f8c99, transparent 50%),
        linear-gradient(135deg, #111827, #18394a);
    }

    .hero .etiqueta {
      color: #76e3df;
      text-transform: uppercase;
      font-size: 12px;
      font-weight: bold;
      letter-spacing: 3px;
    }

    .hero h1 {
      font-size: clamp(34px, 6vw, 60px);
      margin: 18px 0;
      line-height: 1.08;
    }

    .hero p {
      max-width: 600px;
      margin: 0 auto 26px;
      color: #e0e9f1;
      line-height: 1.7;
    }

    .boton {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 12px 17px;
      border: 0;
      border-radius: 9px;
      text-decoration: none;
      font-weight: bold;
      transition: transform .2s, opacity .2s;
    }

    .boton:hover { transform: translateY(-2px); }

    .principal { background: var(--acento); color: white; }
    .whatsapp { background: var(--verde); color: #082b17; }
    .secundario { background: #e8eef3; color: var(--texto); }

    .contenedor {
      width: min(1150px, 100%);
      margin: auto;
      padding: 45px 20px;
    }

    .titulo-seccion {
      text-align: center;
      margin-bottom: 28px;
    }

    .titulo-seccion h2 {
      margin: 0 0 10px;
      font-size: clamp(25px, 4vw, 35px);
    }

    .titulo-seccion p {
      color: #657084;
      line-height: 1.6;
      margin: 0;
    }

    .categorias {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
      margin: 25px 0;
    }

    .filtro {
      border: 1px solid var(--borde);
      background: white;
      border-radius: 30px;
      padding: 10px 17px;
      font-weight: bold;
      color: #334155;
    }

    .filtro.activo, .filtro:hover {
      color: white;
      background: var(--oscuro);
      border-color: var(--oscuro);
    }

    .productos {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 20px;
    }

    .producto {
      background: white;
      border: 1px solid var(--borde);
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 4px 14px #14203408;
      transition: transform .2s, box-shadow .2s;
    }

    .producto:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 25px #14203412;
    }

    .foto-producto {
      width: 100%;
      height: 210px;
      display: block;
      object-fit: cover;
      background: #edf1f5;
      cursor: pointer;
    }

    .producto-info { padding: 16px; }

    .categoria-mini {
      display: inline-block;
      color: var(--acento);
      font-size: 11px;
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: .7px;
      margin-bottom: 8px;
    }

    .producto h3 {
      margin: 0 0 9px;
      font-size: 17px;
    }

    .producto p {
      color: #687386;
      font-size: 13px;
      line-height: 1.5;
      min-height: 39px;
    }

    .precio {
      font-size: 18px;
      font-weight: 800;
      margin: 14px 0;
    }

    .acciones-producto {
      display: grid;
      grid-template-columns: 1fr;
      gap: 8px;
    }

    .acciones-producto .boton { font-size: 13px; }

    .sin-resultados {
      grid-column: 1 / -1;
      text-align: center;
      padding: 35px;
      color: #687386;
    }

    .beneficios {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .beneficio {
      text-align: center;
      padding: 25px 18px;
      border: 1px solid var(--borde);
      border-radius: 14px;
      background: white;
    }

    .beneficio .icono { font-size: 30px; }
    .beneficio h3 { font-size: 17px; }
    .beneficio p { color: #687386; font-size: 14px; line-height: 1.6; }

    .contacto {
      background: #e8eff3;
      border-radius: 18px;
      text-align: center;
      padding: 38px 20px;
    }

    .contacto h2 { margin-top: 0; }

    .contacto p {
      max-width: 560px;
      margin: 12px auto 22px;
      line-height: 1.7;
      color: #566274;
    }

    footer {
      background: var(--oscuro);
      color: #dce4ed;
      text-align: center;
      padding: 28px 18px;
      font-size: 13px;
      line-height: 1.8;
    }

    footer a { color: #76e3df; }

    .wa-flotante {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 25;
      background: #20bd65;
      color: #073519;
      text-decoration: none;
      border-radius: 50px;
      padding: 14px 18px;
      font-weight: 900;
      box-shadow: 0 5px 20px #0003;
    }

    /* Ventana de detalles y galería */

    .modal {
      display: none;
      position: fixed;
      inset: 0;
      z-index: 100;
      padding: 18px;
      background: #08111ddd;
      overflow-y: auto;
      align-items: center;
      justify-content: center;
    }

    .modal.abierto { display: flex; }

    .modal-contenido {
      background: white;
      width: min(850px, 100%);
      border-radius: 18px;
      overflow: hidden;
      position: relative;
      margin: auto;
    }

    .cerrar {
      position: absolute;
      top: 12px;
      right: 12px;
      z-index: 2;
      width: 40px;
      height: 40px;
      border: 0;
      border-radius: 50%;
      background: white;
      box-shadow: 0 2px 12px #0002;
      font-size: 24px;
    }

    .detalle-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }

    .galeria { padding: 20px; background: #f1f4f7; }

    .foto-principal {
      width: 100%;
      height: 330px;
      object-fit: contain;
      display: block;
      background: white;
      border-radius: 12px;
    }

    .miniaturas {
      display: flex;
      gap: 9px;
      overflow-x: auto;
      margin-top: 12px;
      padding-bottom: 5px;
    }

    .miniatura {
      flex: 0 0 72px;
      height: 72px;
      border: 2px solid transparent;
      border-radius: 8px;
      padding: 2px;
      background: white;
      overflow: hidden;
    }

    .miniatura.seleccionada { border-color: var(--acento); }

    .miniatura img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .detalle-info { padding: 32px 25px; }

    .detalle-info h2 {
      font-size: 27px;
      margin: 10px 0;
    }

    .detalle-info p {
      color: #5f6b7c;
      line-height: 1.7;
    }

    .detalle-info ul {
      padding-left: 20px;
      line-height: 1.9;
      color: #465365;
    }

    .referencia {
      display: inline-block;
      margin-top: 14px;
      font-size: 13px;
      color: var(--acento);
    }

    @media (max-width: 850px) {
      .productos { grid-template-columns: repeat(2, minmax(0, 1fr)); }
      .foto-producto { height: 190px; }
    }

    @media (max-width: 600px) {
      .nav { min-height: 62px; }
      .hamburguesa { display: block; }

      .enlaces {
        display: none;
        position: absolute;
        left: 0;
        right: 0;
        top: 62px;
        background: var(--oscuro);
        padding: 18px 22px 22px;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
      }

      .en
