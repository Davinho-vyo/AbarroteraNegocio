<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Tiendita</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body { 
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #3B82F6, #1E40AF);
            color: white;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container { 
            max-width: 400px; 
            margin: 0 auto;
            text-align: center;
        }
        
        h1 { 
            font-size: 2.5em; 
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .subtitle {
            font-size: 1.2em;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .button {
            background: linear-gradient(135deg, #10B981, #059669);
            color: white;
            padding: 25px 20px;
            margin: 15px 0;
            border: none;
            border-radius: 20px;
            font-size: 20px;
            font-weight: bold;
            width: 100%;
            cursor: pointer;
            box-shadow: 0 8px 15px rgba(0,0,0,0.2);
            transition: transform 0.2s, box-shadow 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .button:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 20px rgba(0,0,0,0.3);
        }
        
        .button:active {
            transform: translateY(0);
        }
        
        .button.blue { background: linear-gradient(135deg, #3B82F6, #1E40AF); }
        .button.purple { background: linear-gradient(135deg, #8B5CF6, #6D28D9); }
        .button.yellow { background: linear-gradient(135deg, #F59E0B, #D97706); }
        
        .resumen {
            margin-top: 40px;
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.2);
        }
        
        .resumen h3 {
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 15px;
        }
        
        .stat {
            background: rgba(255,255,255,0.1);
            padding: 15px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.1);
        }
        
        .stat-value {
            font-size: 1.5em;
            font-weight: bold;
            color: #FDE047;
        }
        
        .icon {
            font-size: 1.5em;
        }
        
        .help-btn {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #F59E0B;
            color: white;
            border: none;
            padding: 15px;
            border-radius: 50%;
            font-size: 1.2em;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }
        
        @media (max-width: 480px) {
            .container { padding: 10px; }
            h1 { font-size: 2em; }
            .button { padding: 20px; font-size: 18px; }
        }
    </style>
</head>
<body>
    <button class="help-btn" onclick="mostrarAyuda()">❓</button>
    
    <div class="container">
        <h1>🏪 Mi Tiendita</h1>
        <p class="subtitle">¡Hola Doña María! ¿Qué vamos a hacer hoy?</p>
        
        <button class="button" onclick="registrarVenta()">
            <span class="icon">🛒</span>
            <span>Registrar Venta</span>
        </button>
        
        <button class="button blue" onclick="verInventario()">
            <span class="icon">📦</span>
            <span>Ver mi Inventario</span>
        </button>
        
        <button class="button purple" onclick="listaCompras()">
            <span class="icon">📋</span>
            <span>¿Qué debo comprar?</span>
        </button>
        
        <button class="button yellow" onclick="miDinero()">
            <span class="icon">💰</span>
            <span>Mi Dinero del Día</span>
        </button>
        
        <div class="resumen">
            <h3>📊 Resumen de Hoy</h3>
            <div class="stats">
                <div class="stat">
                    <div>Ventas</div>
                    <div class="stat-value">$0.00</div>
                </div>
                <div class="stat">
                    <div>Ganancias</div>
                    <div class="stat-value">$0.00</div>
                </div>
            </div>
            <p style="margin-top: 15px; font-size: 0.9em; opacity: 0.8;">
                Productos: 5 | Alertas: 0 | Nivel: 1
            </p>
        </div>
    </div>

    <script>
        function registrarVenta() {
            alert('🛒 ¡Registrando venta!\n\nEsta funcionalidad estará disponible pronto.\n\n¡Gracias por probar Mi Tiendita!');
        }
        
        function verInventario() {
            alert('📦 ¡Viendo inventario!\n\nProductos disponibles:\n• Coca-Cola: 24 unidades\n• Sabritas: 15 unidades\n• Pan Bimbo: 8 unidades\n• Leche Lala: 12 unidades');
        }
        
        function listaCompras() {
            alert('📋 ¡Lista de compras!\n\nProductos recomendados:\n• Más refrescos\n• Botanas variadas\n• Pan fresco\n• Productos de limpieza');
        }
        
        function miDinero() {
            alert('💰 ¡Mi dinero del día!\n\nVentas de hoy: $0.00\nGanancias: $0.00\nPromedio por venta: $0.00\n\n¡Empieza a registrar ventas!');
        }
        
        function mostrarAyuda() {
            alert('💡 ¡Ayuda de Mi Tiendita!\n\n🛒 Registra tus ventas diarias\n📦 Controla tu inventario\n📋 Planifica tus compras\n💰 Calcula tus ganancias\n\n¡Hecho especialmente para tenderos mexicanos!');
        }
        
        // Mensaje de bienvenida
        window.onload = function() {
            setTimeout(function() {
                alert('¡Bienvenido a Mi Tiendita! 🏪\n\nEsta es una demostración de tu app.\n\nPuedes probar todos los botones.\n\n¡Pronto tendrás la versión completa!');
            }, 1000);
        }
    </script>
</body>
</html>
