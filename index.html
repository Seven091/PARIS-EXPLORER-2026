<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paris Explorer - Énigmes & Monuments</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- React & ReactDOM -->
    <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <!-- Babel standalone -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
</head>
<body class="bg-slate-100 text-slate-800 select-none overflow-x-hidden font-sans">

    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;

        // Base d'énigmes et défis liés aux monuments parisiens
        const DEFIS_INITIAL = [
            {
                id: '1',
                title: '📐 Le Mystère de la Pyramide',
                monument: 'Musée du Louvre',
                desc: 'Compte le nombre de petites pyramides de verre qui entourent la grande Pyramide du Louvre. Multiplie ce nombre par 10 pour trouver les points !',
                points: 50,
                target: 'Enfant',
                reponse: '3'
            },
            {
                id: '2',
                title: '🦁 Le Secret des Chimères',
                monument: 'Notre-Dame / Parvis',
                desc: 'Au kilomètre Zéro de France (devant Notre-Dame), trouve la rosace en bronze au sol. Quelle phrase ou symbole y est gravé ?',
                points: 40,
                target: 'Famille',
            },
            {
                id: '3',
                title: '🧱 Les Rivets de la Tour Eiffel',
                monument: 'Champs de Mars',
                desc: 'Ado : Trouve le pilier de la Tour Eiffel où est inscrit le nom d\'un célèbre savant français (ex: Ampère, Eiffel, Fourier...). Prends une photo du nom !',
                points: 60,
                target: 'Ado',
            },
            {
                id: '4',
                title: '⛵ La Flotte du Luxembourg',
                monument: 'Jardin du Luxembourg',
                desc: 'Trouve le grand bassin. Combien de voiliers en bois voguent actuellement sur l\'eau ? Fais une course de bateaux en famille !',
                points: 30,
                target: 'Enfant',
            },
            {
                id: '5',
                title: '🎨 Le Mur des Je t\'aime',
                monument: 'Montmartre (Square Jehan Rictus)',
                desc: 'Trouve la phrase "Je t\'aime" écrite dans une langue rare ou insolite sur le mur bleu. Écris-la sur un papier !',
                points: 50,
                target: 'Famille',
            },
            {
                id: '6',
                title: '🏛️ L\'Horloge du Temps',
                monument: 'Musée d\'Orsay',
                desc: 'Observe la grande horloge dorée sur la façade (ou à l\'intérieur). Quel animal ou sculpture la surmonte ?',
                points: 40,
                target: 'Ado',
            },
            {
                id: '7',
                title: '🐲 Le Dragon du Palais-Royal',
                monument: 'Jardin du Palais-Royal',
                desc: 'Trouve les colonnes de Buren. Fais une photo originale où toute la famille est perchée sur des colonnes de hauteurs différentes !',
                points: 50,
                target: 'Famille',
            },
            {
                id: '8',
                title: '🔑 Le Code Caché du Pont des Arts',
                monument: 'Pont des Arts',
                desc: 'Trouve un cadenas ou une inscription originale laissée sur le pont avec une date précise. Quel est l\'an le plus ancien ?',
                points: 40,
                target: 'Ado',
            },
            {
                id: '9',
                title: '📜 La Devise de l\'Hôtel de Ville',
                monument: 'Place de l\'Hôtel de Ville',
                desc: 'Retrouve les 3 mots de la devise de la France sculptés au-dessus de la porte principale.',
                points: 30,
                target: 'Enfant',
            },
            {
                id: '10',
                title: '📵 Traversée des Tuileries',
                monument: 'Jardin des Tuileries',
                desc: 'DÉFI FAMILLE : Marchez de l\'Arc de Triomphe du Carrousel jusqu\'à la Place de la Concorde sans aucun téléphone sorti pendant 20 min !',
                points: 100,
                target: 'Famille',
            },
            {
                id: '11',
                title: '☕ Le Café des Philosophers',
                monument: 'Saint-Germain-des-Prés',
                desc: 'L\'Ado doit commander un jus ou un chocolat chaud au serveur du Café de Flore ou Les Deux Magots avec la formule de politesse parfaite.',
                points: 60,
                target: 'Ado',
            },
            {
                id: '12',
                title: '🕊️ L\'Envol de la Fontaine',
                monument: 'Fontaine St-Michel',
                desc: 'Quel archange est sculpté en train de terrasser le dragon sur la fontaine géante ?',
                points: 40,
                target: 'Enfant',
            }
        ];

        const Icon = ({ name, className = "w-5 h-5" }) => {
            useEffect(() => {
                if (window.lucide) {
                    window.lucide.createIcons();
                }
            }, [name]);
            return <i data-lucide={name} className={className}></i>;
        };

        const App = () => {
            const [defis] = useState(DEFIS_INITIAL);
            const [completed, setCompleted] = useState([]);
            const [score, setScore] = useState(0);
            const [filter, setFilter] = useState('Tous');

            useEffect(() => {
                const savedCompleted = localStorage.getItem('pe_monuments_completed');
                const savedScore = localStorage.getItem('pe_monuments_score');
                if (savedCompleted) setCompleted(JSON.parse(savedCompleted));
                if (savedScore) setScore(Number(savedScore));
            }, []);

            const saveProgress = (newCompleted, newScore) => {
                setCompleted(newCompleted);
                setScore(newScore);
                localStorage.setItem('pe_monuments_completed', JSON.stringify(newCompleted));
                localStorage.setItem('pe_monuments_score', newScore.toString());
            };

            const validerDefi = (item) => {
                if (completed.includes(item.id)) return;
                const newCompleted = [...completed, item.id];
                const newScore = score + item.points;
                saveProgress(newCompleted, newScore);
            };

            const resetGame = () => {
                if (confirm("Réinitialiser les scores et énigmes de la famille ?")) {
                    saveProgress([], 0);
                }
            };

            const defisFiltres = defis.filter((d) => {
                if (filter === 'Tous') return true;
                return d.target === filter;
            });

            return (
                <div className="flex flex-col min-h-screen bg-slate-100 max-w-md mx-auto shadow-2xl relative border-x border-slate-200">
                    
                    {/* Header */}
                    <header className="bg-[#1D3557] text-white pt-10 pb-8 px-6 text-center rounded-b-[2.5rem] shadow-lg relative">
                        <p className="text-[#A8DADC] text-[11px] font-extrabold tracking-widest uppercase mb-1">
                            PARIS EXPLORER • MONUMENTS
                        </p>
                        <h1 className="text-4xl font-black text-amber-400 my-2 flex items-center justify-center gap-2">
                            <span>🏆</span> {score} <span className="text-lg font-bold text-white">PTS</span>
                        </h1>
                        <p className="text-slate-200 text-xs font-semibold bg-white/10 py-1.5 px-4 rounded-full inline-block mt-1">
                            {completed.length} / {defis.length} Énigmes résolues
                        </p>

                        <button 
                            onClick={resetGame}
                            className="absolute top-4 right-4 text-slate-400 hover:text-white p-2"
                            title="Réinitialiser"
                        >
                            <Icon name="rotate-ccw" className="w-4 h-4" />
                        </button>
                    </header>

                    {/* Filtres */}
                    <nav className="flex justify-around bg-white p-3 shadow-md my-4 mx-4 rounded-2xl border border-slate-100">
                        {['Tous', 'Ado', 'Enfant', 'Famille'].map((f) => {
                            const isActive = filter === f;
                            const label = f === 'Ado' ? '⚡ Ado' : f === 'Enfant' ? '🎈 Enfant' : f === 'Famille' ? '👨‍👩‍👧‍👦 Famille' : 'Tous';
                            return (
                                <button
                                    key={f}
                                    onClick={() => setFilter(f)}
                                    className={`py-2 px-3.5 rounded-xl text-xs font-bold transition-all ${
                                        isActive 
                                            ? 'bg-[#1D3557] text-white shadow-sm' 
                                            : 'bg-slate-100 text-slate-500 hover:bg-slate-200'
                                    }`}
                                >
                                    {label}
                                </button>
                            );
                        })}
                    </nav>

                    {/* Liste d'énigmes */}
                    <main className="flex-1 px-4 pb-12 space-y-4">
                        {defisFiltres.map((item) => {
                            const isDone = completed.includes(item.id);
                            return (
                                <div 
                                    key={item.id} 
                                    className={`p-5 rounded-2xl border transition-all ${
                                        isDone 
                                            ? 'bg-emerald-50/90 border-emerald-300 shadow-none opacity-80' 
                                            : 'bg-white border-slate-200 shadow-sm'
                                    }`}
                                >
                                    <div className="flex justify-between items-start gap-3 mb-1">
                                        <h3 className="font-extrabold text-base text-[#1D3557] leading-snug">
                                            {item.title}
                                        </h3>
                                        <span className="bg-[#E63946] text-white font-black text-xs px-2.5 py-1 rounded-lg shrink-0">
                                            +{item.points} pts
                                        </span>
                                    </div>

                                    <div className="inline-flex items-center gap-1 text-[11px] font-bold text-amber-600 bg-amber-50 px-2.5 py-0.5 rounded-md mb-3 border border-amber-200/60">
                                        <Icon name="map-pin" className="w-3 h-3" />
                                        <span>{item.monument}</span>
                                    </div>

                                    <p className="text-slate-600 text-xs leading-relaxed mb-4">
                                        {item.desc}
                                    </p>

                                    <div className="flex justify-between items-center pt-3 border-t border-slate-100">
                                        <span className="text-[11px] font-bold text-slate-400 uppercase tracking-wider">
                                            Cible : <span className="text-[#1D3557]">{item.target}</span>
                                        </span>

                                        <button
                                            disabled={isDone}
                                            onClick={() => validerDefi(item)}
                                            className={`py-2.5 px-4 rounded-xl font-bold text-xs uppercase tracking-wider transition-transform active:scale-95 ${
                                                isDone 
                                                    ? 'bg-[#2A9D8F] text-white cursor-default' 
                                                    : 'bg-[#1D3557] text-white hover:bg-slate-800 shadow-md shadow-[#1D3557]/20'
                                            }`}
                                        >
                                            {isDone ? 'Résolu ✓' : 'Valider l\'énigme'}
                                        </button>
                                    </div>
                                </div>
                            );
                        })}
                    </main>

                </div>
            );
        };

        ReactDOM.createRoot(document.getElementById('root')).render(<App />);
    </script>
</body>
</html>

