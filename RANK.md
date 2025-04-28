
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ranking de Lucros Completo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .rank-badge {
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-weight: bold;
            color: white;
        }
        
        .rank-1 {
            background: linear-gradient(135deg, #FFD700 0%, #DAA520 100%);
            box-shadow: 0 4px 8px rgba(218, 165, 32, 0.3);
        }
        
        .rank-2 {
            background: linear-gradient(135deg, #C0C0C0 0%, #A8A8A8 100%);
            box-shadow: 0 4px 8px rgba(168, 168, 168, 0.3);
        }
        
        .rank-3 {
            background: linear-gradient(135deg, #CD7F32 0%, #A0522D 100%);
            box-shadow: 0 4px 8px rgba(160, 82, 45, 0.3);
        }
        
        .rank-4, .rank-5 {
            background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
            box-shadow: 0 4px 8px rgba(41, 128, 185, 0.3);
        }
        
        .rank-other {
            background: linear-gradient(135deg, #95a5a6 0%, #7f8c8d 100%);
            box-shadow: 0 4px 8px rgba(127, 140, 141, 0.3);
        }
        
        .profit-bar {
            height: 8px;
            border-radius: 4px;
            background: linear-gradient(90deg, #4facfe 0%, #00f2fe 100%);
            transition: all 0.3s ease;
        }
        
        .profit-bar:hover {
            transform: scaleY(1.5);
        }
        
        .card {
            backdrop-filter: blur(10px);
            background: rgba(255, 255, 255, 0.8);
            transition: all 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .highlight {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255, 215, 0, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(255, 215, 0, 0); }
            100% { box-shadow: 0 0 0 0 rgba(255, 215, 0, 0); }
        }
        
        .hidden-rows {
            display: none;
        }
        
        .toggle-rows {
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .toggle-rows:hover {
            background-color: #f0f4f8;
        }
        
        .rotate-arrow {
            transform: rotate(180deg);
        }
    </style>
</head>
<body class="py-8 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
        <!-- Header Section -->
        <div class="text-center mb-10">
            <h1 class="text-3xl font-bold text-gray-800 mb-2">Ranking de Lucros Completo</h1>
            <p class="text-gray-600">Visualização detalhada de todos os desempenhos</p>
            <div class="mt-4 flex justify-center space-x-4">
                <span class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-medium">Atualizado hoje</span>
                <span class="px-3 py-1 bg-green-100 text-green-800 rounded-full text-sm font-medium">+12% em relação ao mês passado</span>
            </div>
        </div>
        
        <!-- Top Performers -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
            <!-- 2nd Place -->
            <div class="card p-6 rounded-xl shadow-md flex flex-col items-center">
                <div class="rank-badge rank-2 mb-4">2</div>
                <div class="text-center mb-4">
                    <h3 class="text-xl font-semibold text-gray-800">TALYSON</h3>
                    <p class="text-gray-600">R$ 5.686,00</p>
                </div>
                <div class="w-full bg-gray-200 rounded-full h-2 mb-2">
                    <div class="profit-bar rounded-full h-2" style="width: 85%"></div>
                </div>
                <div class="text-xs text-gray-500 mt-2">85% da meta mensal</div>
                <div class="mt-4 flex space-x-2">
                    <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded-full text-xs">Top performer</span>
                </div>
            </div>
            
            <!-- 1st Place (Highlighted) -->
            <div class="card p-6 rounded-xl shadow-lg highlight flex flex-col items-center relative">
                <div class="absolute top-0 right-0 mt-2 mr-2">
                    <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs font-bold">LÍDER</span>
                </div>
                <div class="rank-badge rank-1 mb-4">1</div>
                <div class="text-center mb-4">
                    <h3 class="text-2xl font-bold text-gray-800">FLAVIN</h3>
                    <p class="text-gray-600 font-medium">R$ 6.546,60</p>
                </div>
                <div class="w-full bg-gray-200 rounded-full h-2 mb-2">
                    <div class="profit-bar rounded-full h-2" style="width: 98%"></div>
                </div>
                <div class="text-xs text-gray-500 mt-2">98% da meta mensal</div>
                <div class="mt-4 flex space-x-2">
                    <span class="px-2 py-1 bg-green-100 text-green-800 rounded-full text-xs">Recorde</span>
                    <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">+15%</span>
                </div>
            </div>
            
            <!-- 3rd Place -->
            <div class="card p-6 rounded-xl shadow-md flex flex-col items-center">
                <div class="rank-badge rank-3 mb-4">3</div>
                <div class="text-center mb-4">
                    <h3 class="text-xl font-semibold text-gray-800">LUCAS PRAXEDES</h3>
                    <p class="text-gray-600">R$ 4.227,00</p>
                </div>
                <div class="w-full bg-gray-200 rounded-full h-2 mb-2">
                    <div class="profit-bar rounded-full h-2" style="width: 63%"></div>
                </div>
                <div class="text-xs text-gray-500 mt-2">63% da meta mensal</div>
                <div class="mt-4 flex space-x-2">
                    <span class="px-2 py-1 bg-orange-100 text-orange-800 rounded-full text-xs">Em crescimento</span>
                </div>
            </div>
        </div>
        
        <!-- Full Ranking Table -->
        <div class="bg-white rounded-xl shadow-md overflow-hidden">
            <div class="px-6 py-4 border-b border-gray-200">
                <h2 class="text-lg font-semibold text-gray-800">Ranking Completo</h2>
            </div>
            <div class="divide-y divide-gray-200">
                <!-- Table Header -->
                <div class="grid grid-cols-12 gap-4 px-6 py-3 bg-gray-50 text-xs font-medium text-gray-500 uppercase tracking-wider">
                    <div class="col-span-1">Rank</div>
                    <div class="col-span-5">Nome</div>
                    <div class="col-span-4">Lucro</div>
                    <div class="col-span-2">Status</div>
                </div>
                
                <!-- Top 6 Rows (Visible by default) -->
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-1">1</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">FLAVIN</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 6.546,60</span>
                            <span class="text-green-500 text-xs">+15%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 98%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-green-100 text-green-800 rounded-full text-xs">Líder</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-2">2</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">TALYSON</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 5.686,00</span>
                            <span class="text-green-500 text-xs">+10%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 85%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded-full text-xs">Top performer</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-3">3</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">LUCAS PRAXEDES</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 4.227,00</span>
                            <span class="text-green-500 text-xs">+8%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 63%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-orange-100 text-orange-800 rounded-full text-xs">Crescendo</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-4">4</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">GHOST</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 3.874,00</span>
                            <span class="text-green-500 text-xs">+12%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 58%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Consistente</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-4">4</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">KLEITON</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 1.396,00</span>
                            <span class="text-green-500 text-xs">+8%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 21%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">Regular</span>
                    </div>
                </div>
                
                <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                    <div class="col-span-1">
                        <div class="rank-badge rank-4">4</div>
                    </div>
                    <div class="col-span-5 font-medium text-gray-800">ARLYSON</div>
                    <div class="col-span-4">
                        <div class="flex items-center">
                            <span class="text-gray-700 mr-2">R$ 944,00</span>
                            <span class="text-red-500 text-xs">-5%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                            <div class="profit-bar h-1.5 rounded-full" style="width: 14%"></div>
                        </div>
                    </div>
                    <div class="col-span-2">
                        <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Atenção</span>
                    </div>
                </div>
                
                <!-- Hidden Rows (Will be shown when toggle is clicked) -->
                <div id="hidden-rows" class="hidden-rows">
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-5">5</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">RODRIGO</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 1.424,00</span>
                                <span class="text-green-500 text-xs">+22%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 21%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-green-100 text-green-800 rounded-full text-xs">Crescendo</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-5">5</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">CAUAN</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 1.104,00</span>
                                <span class="text-green-500 text-xs">+15%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 17%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-5">5</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">MATHUES</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 1.042,00</span>
                                <span class="text-red-500 text-xs">-3%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 16%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">Regular</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">6</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">MENDOÇA</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 811,00</span>
                                <span class="text-green-500 text-xs">+7%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 12%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">7</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">FERNANDO RZ</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 1.061,00</span>
                                <span class="text-green-500 text-xs">+9%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 16%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">8</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">MATARINO</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 540,00</span>
                                <span class="text-red-500 text-xs">-2%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 8%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">Regular</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">9</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">KENOBI</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 480,00</span>
                                <span class="text-red-500 text-xs">-8%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 7%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Atenção</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">10</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">SANTANA</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 594,00</span>
                                <span class="text-green-500 text-xs">+5%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 9%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">11</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">R AZEVEDO</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 413,00</span>
                                <span class="text-red-500 text-xs">-4%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 6%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">Regular</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">12</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">LEONARDO</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 275,00</span>
                                <span class="text-green-500 text-xs">+3%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 4%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">13</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">JOAOYZ</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 237,00</span>
                                <span class="text-red-500 text-xs">-6%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 4%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">Regular</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">14</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">G7</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 372,00</span>
                                <span class="text-green-500 text-xs">+2%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 6%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Estável</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">15</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">CABELINHO</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 136,00</span>
                                <span class="text-red-500 text-xs">-9%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 2%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Atenção</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">16</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">CAUE</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 40,00</span>
                                <span class="text-red-500 text-xs">-12%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 1%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Crítico</span>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-12 gap-4 px-6 py-4 items-center hover:bg-gray-50 transition-colors">
                        <div class="col-span-1">
                            <div class="rank-badge rank-other">17</div>
                        </div>
                        <div class="col-span-5 font-medium text-gray-800">SHURK</div>
                        <div class="col-span-4">
                            <div class="flex items-center">
                                <span class="text-gray-700 mr-2">R$ 27,00</span>
                                <span class="text-red-500 text-xs">-15%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-1.5 mt-1">
                                <div class="profit-bar h-1.5 rounded-full" style="width: 0.5%"></div>
                            </div>
                        </div>
                        <div class="col-span-2">
                            <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Crítico</span>
                        </div>
                    </div>
                </div>
                
                <!-- Toggle Rows Button -->
                <div id="toggle-rows" class="toggle-rows grid grid-cols-12 gap-4 px-6 py-4 items-center bg-gray-50 text-center">
                    <div class="col-span-12 flex justify-center items-center">
                        <span class="text-blue-600 font-medium mr-2">Mostrar todos os participantes</span>
                        <i class="fas fa-chevron-down text-blue-600 transition-transform duration-300" id="toggle-arrow"></i>
                    </div>
                </div>
            </div>
            
            <!-- Table Footer -->
            <div class="px-6 py-4 bg-gray-50 text-right">
                <button class="px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors">
                    Exportar Relatório
                </button>
            </div>
        </div>
        
        <!-- Performance Insights -->
        <div class="mt-8 grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="card p-6 rounded-xl shadow-md">
                <div class="flex items-center mb-4">
                    <div class="p-3 bg-blue-100 rounded-lg mr-4">
                        <i class="fas fa-trophy text-blue-600"></i>
                    </div>
                    <div>
                        <h3 class="font-semibold text-gray-800">Líder do Mês</h3>
                        <p class="text-sm text-gray-600">FLAVIN com R$ 6.546,60</p>
                    </div>
                </div>
                <p class="text-sm text-gray-600">Atingiu 98% da meta mensal, estabelecendo um novo recorde para a equipe.</p>
            </div>
            
            <div class="card p-6 rounded-xl shadow-md">
                <div class="flex items-center mb-4">
                    <div class="p-3 bg-green-100 rounded-lg mr-4">
                        <i class="fas fa-chart-line text-green-600"></i>
                    </div>
                    <div>
                        <h3 class="font-semibold text-gray-800">Maior Crescimento</h3>
                        <p class="text-sm text-gray-600">RODRIGO +22%</p>
                    </div>
                </div>
                <p class="text-sm text-gray-600">Destacou-se pelo maior crescimento percentual em relação ao mês anterior.</p>
            </div>
            
            <div class="card p-6 rounded-xl shadow-md">
                <div class="flex items-center mb-4">
                    <div class="p-3 bg-purple-100 rounded-lg mr-4">
                        <i class="fas fa-users text-purple-600"></i>
                    </div>
                    <div>
                        <h3 class="font-semibold text-gray-800">Desempenho Geral</h3>
                        <p class="text-sm text-gray-600">+12% em relação ao mês passado</p>
                    </div>
                </div>
                <p class="text-sm text-gray-600">A equipe como um todo apresentou um crescimento significativo nos resultados.</p>
            </div>
        </div>
        
        <!-- Comments Section -->
        <div class="mt-10 card p-6 rounded-xl shadow-md">
            <h2 class="text-lg font-semibold text-gray-800 mb-4">Análise do Desempenho</h2>
            
            <div class="mb-6">
                <h3 class="font-medium text-gray-800 mb-2">Destaques Positivos</h3>
                <ul class="list-disc pl-5 space-y-2 text-sm text-gray-600">
                    <li>FLAVIN se mantém como líder absoluto com um lucro impressionante de R$ 6.546,60</li>
                    <li>TALYSON em segundo lugar com R$ 5.686,00, mostrando consistência no topo</li>
                    <li>RODRIGO apresentou o maior crescimento (+22%) entre os membros da equipe</li>
                    <li>O desempenho geral da equipe foi 12% melhor que no mês anterior</li>
                </ul>
            </div>
            
            <div class="mb-6">
                <h3 class="font-medium text-gray-800 mb-2">Oportunidades de Melhoria</h3>
                <ul class="list-disc pl-5 space-y-2 text-sm text-gray-600">
                    <li>ARLYSON apresentou queda de 5% no desempenho em relação ao mês anterior</li>
                    <li>MATHUES também teve uma pequena redução de 3% nos resultados</li>
                    <li>Alguns membros como SHURK (R$ 27,00) e CAUE (R$ 40,00) precisam de atenção especial</li>
                </ul>
            </div>
            
            <div>
                <h3 class="font-medium text-gray-800 mb-2">Recomendações</h3>
                <ul class="list-disc pl-5 space-y-2 text-sm text-gray-600">
                    <li>Implementar programa de mentoria entre os top performers e os que estão com dificuldades</li>
                    <li>Analisar as estratégias de FLAVIN e TALYSON para replicar para toda a equipe</li>
                    <li>Realizar treinamentos específicos para os membros com desempenho abaixo da média</li>
                </ul>
            </div>
        </div>
    </div>
    
    <script>
        // Toggle hidden rows
        const toggleRows = document.getElementById('toggle-rows');
        const hiddenRows = document.getElementById('hidden-rows');
        const toggleArrow = document.getElementById('toggle-arrow');
        
        toggleRows.addEventListener('click', () => {
            hiddenRows.classList.toggle('hidden-rows');
            toggleArrow.classList.toggle('rotate-arrow');
            
            if (hiddenRows.classList.contains('hidden-rows')) {
                toggleRows.querySelector('span').textContent = 'Mostrar todos os participantes';
            } else {
                toggleRows.querySelector('span').textContent = 'Ocultar participantes';
            }
        });
        
        // Simple animation for the leader card
        const leaderCard = document.querySelector('.highlight');
        
        leaderCard.addEventListener('mouseenter', () => {
            leaderCard.classList.add('shadow-lg');
        });
        
        leaderCard.addEventListener('mouseleave', () => {
            leaderCard.classList.remove('shadow-lg');
        });
        
        // Add click effect to table rows
        const tableRows = document.querySelectorAll('.grid.grid-cols-12');
        
        tableRows.forEach(row => {
            row.addEventListener('click', () => {
                // Remove active class from all rows
                tableRows.forEach(r => r.classList.remove('bg-blue-50'));
                // Add active class to clicked row
                row.classList.add('bg-blue-50');
                
                // In a real app, you might fetch more details here
                console.log('Selected:', row.querySelector('.font-medium').textContent);
            });
        });
    </script>
</body>
</html>
