import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Trophy, Gift, Dumbbell, Bike, Star, Medal, Smartphone, Users, ShieldCheck } from "lucide-react";
import { motion } from "framer-motion";

export default function PulseClubWebsite() {
  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* HERO SECTION */}
      <section className="relative overflow-hidden bg-gradient-to-r from-black via-zinc-900 to-lime-500 py-20 px-8 lg:px-20">
        <div className="grid lg:grid-cols-2 gap-10 items-center">
          <motion.div
            initial={{ opacity: 0, x: -50 }}
            animate={{ opacity: 1, x: 0 }}
            transition={{ duration: 0.8 }}
          >
            <h1 className="text-6xl font-extrabold leading-tight mb-6">
              PULSE <span className="text-lime-400">CLUB</span>
            </h1>

            <p className="text-2xl text-zinc-300 mb-8 leading-relaxed">
              Le programme sportif qui récompense votre passion.
              Bougez plus, gagnez plus.
            </p>

            <div className="flex gap-4 flex-wrap">
              <Button className="bg-lime-400 hover:bg-lime-500 text-black text-lg px-8 py-6 rounded-2xl font-bold">
                Rejoindre le club
              </Button>

              <Button
                variant="outline"
                className="border-lime-400 text-lime-400 hover:bg-lime-400 hover:text-black text-lg px-8 py-6 rounded-2xl"
              >
                Découvrir
              </Button>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, scale: 0.9 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 0.8 }}
            className="relative"
          >
            <div className="bg-zinc-900 p-8 rounded-[40px] border border-lime-400 shadow-2xl">
              <div className="bg-black rounded-3xl p-8">
                <h2 className="text-3xl font-bold mb-6 text-lime-400">
                  Vos récompenses
                </h2>

                <div className="space-y-6">
                  <div className="flex items-center justify-between bg-zinc-800 p-4 rounded-2xl">
                    <div className="flex items-center gap-3">
                      <Gift className="text-lime-400" />
                      <span>Points actuels</span>
                    </div>
                    <span className="font-bold text-2xl">12 450</span>
                  </div>

                  <div className="flex items-center justify-between bg-zinc-800 p-4 rounded-2xl">
                    <div className="flex items-center gap-3">
                      <Medal className="text-yellow-400" />
                      <span>Niveau</span>
                    </div>
                    <span className="font-bold text-2xl text-yellow-400">GOLD</span>
                  </div>

                  <div className="w-full bg-zinc-700 rounded-full h-4 overflow-hidden">
                    <div className="bg-lime-400 h-full w-[78%] rounded-full"></div>
                  </div>
                </div>
              </div>
            </div>
          </motion.div>
        </div>
      </section>

      {/* NAVIGATION */}
      <section className="sticky top-0 z-50 bg-black border-b border-zinc-800">
        <div className="flex justify-center gap-10 py-5 text-lg font-semibold">
          <a href="#accueil" className="hover:text-lime-400 transition">Accueil</a>
          <a href="#recompenses" className="hover:text-lime-400 transition">Récompenses</a>
          <a href="#activites" className="hover:text-lime-400 transition">Activités</a>
          <a href="#contact" className="hover:text-lime-400 transition">Contact</a>
        </div>
      </section>

      {/* PAGE 1 */}
      <section id="accueil" className="py-24 px-8 lg:px-20 bg-zinc-950">
        <div className="text-center mb-16">
          <h2 className="text-5xl font-extrabold mb-6">
            Comment ça <span className="text-lime-400">fonctionne</span> ?
          </h2>

          <p className="text-zinc-400 text-xl max-w-3xl mx-auto leading-relaxed">
            Achetez, bougez, cumulez des points et débloquez des avantages exclusifs.
            Chaque activité sportive vous rapproche de nouvelles récompenses.
          </p>
        </div>

        <div className="grid md:grid-cols-3 gap-8">
          <Card className="bg-zinc-900 border border-zinc-800 rounded-3xl">
            <CardContent className="p-8">
              <Dumbbell className="w-14 h-14 text-lime-400 mb-6" />
              <h3 className="text-3xl font-bold mb-4">Bougez</h3>
              <p className="text-zinc-400 leading-relaxed">
                Courez, faites du vélo, allez à la salle ou participez à des défis sportifs.
              </p>
            </CardContent>
          </Card>

          <Card className="bg-zinc-900 border border-zinc-800 rounded-3xl">
            <CardContent className="p-8">
              <Gift className="w-14 h-14 text-lime-400 mb-6" />
              <h3 className="text-3xl font-bold mb-4">Gagnez</h3>
              <p className="text-zinc-400 leading-relaxed">
                Cumulez des points à chaque achat et activité physique réalisée.
              </p>
            </CardContent>
          </Card>

          <Card className="bg-zinc-900 border border-zinc-800 rounded-3xl">
            <CardContent className="p-8">
              <Trophy className="w-14 h-14 text-lime-400 mb-6" />
              <h3 className="text-3xl font-bold mb-4">Profitez</h3>
              <p className="text-zinc-400 leading-relaxed">
                Échangez vos points contre des produits, événements VIP et coaching.
              </p>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* PAGE 2 */}
      <section id="recompenses" className="py-24 px-8 lg:px-20 bg-black">
        <div className="text-center mb-16">
          <h2 className="text-5xl font-extrabold mb-6">
            Les niveaux <span className="text-lime-400">VIP</span>
          </h2>

          <p className="text-zinc-400 text-xl">
            Plus vous êtes actif, plus vos récompenses deviennent exclusives.
          </p>
        </div>

        <div className="grid lg:grid-cols-3 gap-8">
          <Card className="bg-gradient-to-b from-amber-700 to-zinc-900 rounded-3xl border-none shadow-2xl">
            <CardContent className="p-10">
              <h3 className="text-4xl font-extrabold mb-6">BRONZE</h3>
              <ul className="space-y-4 text-lg text-zinc-200">
                <li>✔ Promotions exclusives</li>
                <li>✔ Accès aux ventes privées</li>
                <li>✔ Cadeau d'anniversaire</li>
                <li>✔ Réductions sportives</li>
              </ul>
            </CardContent>
          </Card>

          <Card className="bg-gradient-to-b from-zinc-400 to-zinc-900 rounded-3xl border-none shadow-2xl scale-105">
            <CardContent className="p-10">
              <h3 className="text-4xl font-extrabold mb-6">SILVER</h3>
              <ul className="space-y-4 text-lg text-zinc-200">
                <li>✔ Livraison offerte</li>
                <li>✔ Réductions personnalisées</li>
                <li>✔ Retours prolongés</li>
                <li>✔ Coaching en ligne</li>
              </ul>
            </CardContent>
          </Card>

          <Card className="bg-gradient-to-b from-yellow-500 to-zinc-900 rounded-3xl border-none shadow-2xl">
            <CardContent className="p-10">
              <h3 className="text-4xl font-extrabold mb-6">GOLD</h3>
              <ul className="space-y-4 text-lg text-zinc-200">
                <li>✔ Invitations VIP</li>
                <li>✔ Service client prioritaire</li>
                <li>✔ Produits exclusifs</li>
                <li>✔ Accès anticipé aux collections</li>
              </ul>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* PAGE 3 */}
      <section id="activites" className="py-24 px-8 lg:px-20 bg-zinc-950">
        <div className="text-center mb-16">
          <h2 className="text-5xl font-extrabold mb-6">
            Activités & <span className="text-lime-400">Points</span>
          </h2>

          <p className="text-zinc-400 text-xl">
            Chaque action vous rapporte des points et des récompenses.
          </p>
        </div>

        <div className="grid lg:grid-cols-2 gap-8">
          <Card className="bg-zinc-900 rounded-3xl border border-zinc-800">
            <CardContent className="p-10 space-y-6">
              <div className="flex items-center justify-between text-xl">
                <div className="flex items-center gap-4">
                  <Bike className="text-lime-400" />
                  <span>Sortie vélo</span>
                </div>
                <span className="font-bold">+100 pts</span>
              </div>

              <div className="flex items-center justify-between text-xl">
                <div className="flex items-center gap-4">
                  <Dumbbell className="text-lime-400" />
                  <span>Séance fitness</span>
                </div>
                <span className="font-bold">+80 pts</span>
              </div>

              <div className="flex items-center justify-between text-xl">
                <div className="flex items-center gap-4">
                  <Star className="text-lime-400" />
                  <span>Défi sportif</span>
                </div>
                <span className="font-bold">+150 pts</span>
              </div>
            </CardContent>
          </Card>

          <Card className="bg-lime-400 text-black rounded-3xl border-none shadow-2xl">
            <CardContent className="p-10">
              <h3 className="text-4xl font-extrabold mb-8">
                Bonus écologiques
              </h3>

              <div className="space-y-6 text-xl font-semibold">
                <div className="flex justify-between">
                  <span>Recycler vos produits</span>
                  <span>+300 pts</span>
                </div>

                <div className="flex justify-between">
                  <span>Achat responsable</span>
                  <span>x2 pts</span>
                </div>

                <div className="flex justify-between">
                  <span>Livraison verte</span>
                  <span>+100 pts</span>
                </div>
              </div>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* APPLICATION SECTION */}
      <section className="py-24 px-8 lg:px-20 bg-black">
        <div className="grid lg:grid-cols-2 gap-12 items-center">
          <div>
            <h2 className="text-5xl font-extrabold mb-8 leading-tight">
              Votre passion mérite <span className="text-lime-400">PLUS</span>
            </h2>

            <p className="text-zinc-400 text-xl leading-relaxed mb-8">
              Rejoignez une communauté de sportifs passionnés et profitez d'une
              expérience premium avec des défis, récompenses et événements exclusifs.
            </p>

            <div className="flex gap-6 flex-wrap">
              <Button className="bg-lime-400 hover:bg-lime-500 text-black px-8 py-6 rounded-2xl text-lg font-bold">
                Télécharger l'application
              </Button>

              <Button
                variant="outline"
                className="border-lime-400 text-lime-400 hover:bg-lime-400 hover:text-black px-8 py-6 rounded-2xl text-lg"
              >
                Voir les défis
              </Button>
            </div>
          </div>

          <div className="grid grid-cols-2 gap-6">
            <Card className="bg-zinc-900 rounded-3xl border border-zinc-800">
              <CardContent className="p-8 text-center">
                <Users className="w-14 h-14 mx-auto mb-6 text-lime-400" />
                <h3 className="text-2xl font-bold mb-3">Communauté</h3>
                <p className="text-zinc-400">Des milliers de sportifs connectés.</p>
              </CardContent>
            </Card>

            <Card className="bg-zinc-900 rounded-3xl border border-zinc-800">
              <CardContent className="p-8 text-center">
                <Smartphone className="w-14 h-14 mx-auto mb-6 text-lime-400" />
                <h3 className="text-2xl font-bold mb-3">Application</h3>
                <p className="text-zinc-400">Suivez vos points en temps réel.</p>
              </CardContent>
            </Card>

            <Card className="bg-zinc-900 rounded-3xl border border-zinc-800">
              <CardContent className="p-8 text-center">
                <ShieldCheck className="w-14 h-14 mx-auto mb-6 text-lime-400" />
                <h3 className="text-2xl font-bold mb-3">Sécurité</h3>
                <p className="text-zinc-400">Vos données protégées et sécurisées.</p>
              </CardContent>
            </Card>

            <Card className="bg-zinc-900 rounded-3xl border border-zinc-800">
              <CardContent className="p-8 text-center">
                <Trophy className="w-14 h-14 mx-auto mb-6 text-lime-400" />
                <h3 className="text-2xl font-bold mb-3">Challenges</h3>
                <p className="text-zinc-400">Des défis sportifs chaque semaine.</p>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* FOOTER */}
      <footer id="contact" className="bg-lime-400 text-black py-10 px-8 lg:px-20">
        <div className="grid lg:grid-cols-3 gap-8 items-center">
          <div>
            <h3 className="text-4xl font-extrabold mb-3">PULSE CLUB</h3>
            <p className="text-lg font-medium">
              Bien plus qu'un programme de fidélité sportif.
            </p>
          </div>

          <div className="text-center">
            <p className="text-xl font-bold">contact@pulseclub.fr</p>
            <p className="text-lg">www.pulseclub.fr</p>
          </div>

          <div className="flex justify-end gap-4">
            <Button className="bg-black text-lime-400 hover:bg-zinc-900 rounded-2xl px-6 py-5">
              Instagram
            </Button>

            <Button className="bg-black text-lime-400 hover:bg-zinc-900 rounded-2xl px-6 py-5">
              TikTok
            </Button>
          </div>
        </div>
      </footer>
    </div>
  );
}
