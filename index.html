import React, { useState, useEffect } from "react";
import { motion, AnimatePresence } from "framer-motion";
import {
  Card,
  CardContent,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import {
  Tabs,
  TabsList,
  TabsTrigger,
  TabsContent,
} from "@/components/ui/tabs";
import { Input } from "@/components/ui/input";
import {
  ShieldCheck,
  KeyRound,
  Server,
  HelpCircle,
  RefreshCcw,
} from "lucide-react";
import {
  BarChart,
  Bar,
  XAxis,
  YAxis,
  Tooltip,
  ResponsiveContainer,
} from "recharts";

// Основна функция за оценка на пароли – проста евристика
function calculateStrength(pwd) {
  if (!pwd) return { score: 0, label: "Липсва" };
  let score = 0;
  if (pwd.length >= 8) score += 1;
  if (/[a-z]/.test(pwd) && /[A-Z]/.test(pwd)) score += 1;
  if (/\d/.test(pwd)) score += 1;
  if (/[^A-Za-z0-9]/.test(pwd)) score += 1;

  const labels = ["Слаба", "Средна", "Добра", "Силна"];
  return { score, label: labels[Math.max(score - 1, 0)] };
}

const questions = [
  {
    q: "Кой порт използва HTTPS?",
    options: ["80", "21", "443", "25"],
    a: "443",
  },
  {
    q: "Коя е първата фаза на етичния хак?",
    options: [
      "Експлоатация",
      "Отпечатване (Footprinting)",
      "Поддържане на достъп",
      "Скриване на следи",
    ],
    a: "Отпечатване (Footprinting)",
  },
  {
    q: "Какво означава съкращението VPN?",
    options: [
      "Virtual Public Network",
      "Verified Private Node",
      "Virtual Private Network",
      "Visual Packet Numbering",
    ],
    a: "Virtual Private Network",
  },
];

export default function CyberSecuritySite() {
  const [tab, setTab] = useState("dashboard");

  // Port Scanner
  const [target, setTarget] = useState("");
  const [scanData, setScanData] = useState([]);
  const handleScan = () => {
    const ports = [21, 22, 23, 25, 53, 80, 110, 139, 143, 443, 445, 587, 993, 995];
    const data = ports.map((p) => ({ port: p, status: Math.random() > 0.7 ? "open" : "closed" }));
    setScanData(data);
  };

  // Password Strength
  const [pwd, setPwd] = useState("");
  const strength = calculateStrength(pwd);

  // Quiz
  const [step, setStep] = useState(0);
  const [selected, setSelected] = useState(null);
  const [score, setScore] = useState(0);

  const current = questions[step];

  const handleAnswer = (opt) => {
    setSelected(opt);
    if (opt === current.a) setScore((s) => s + 1);
  };

  const nextQuestion = () => {
    setSelected(null);
    setStep((s) => s + 1);
  };

  // Стили за анимации
  const fade = {
    hidden: { opacity: 0, y: 20 },
    visible: { opacity: 1, y: 0 },
    exit: { opacity: 0, y: -20 },
  };

  return (
    <div className="min-h-screen bg-gray-50 p-4">
      <Card className="max-w-5xl mx-auto shadow-2xl rounded-2xl">
        <CardHeader>
          <CardTitle className="text-3xl flex items-center gap-2 font-bold">
            <ShieldCheck className="w-8 h-8 text-green-600" /> Cyber Security Hub
          </CardTitle>
        </CardHeader>
        <CardContent>
          <Tabs value={tab} onValueChange={setTab} className="w-full">
            <TabsList className="grid grid-cols-4 gap-2">
              <TabsTrigger value="dashboard" className="flex items-center gap-1">
                <Server className="w-4 h-4" /> Табло
              </TabsTrigger>
              <TabsTrigger value="scanner" className="flex items-center gap-1">
                <RefreshCcw className="w-4 h-4" /> Скенер на портове
              </TabsTrigger>
              <TabsTrigger value="password" className="flex items-center gap-1">
                <KeyRound className="w-4 h-4" /> Сила на парола
              </TabsTrigger>
              <TabsTrigger value="quiz" className="flex items-center gap-1">
                <HelpCircle className="w-4 h-4" /> Куиз
              </TabsTrigger>
            </TabsList>

            {/* Dashboard */}
            <TabsContent value="dashboard" className="mt-6">
              <AnimatePresence mode="wait">
                {tab === "dashboard" && (
                  <motion.div
                    key="dash"
                    variants={fade}
                    initial="hidden"
                    animate="visible"
                    exit="exit"
                    className="space-y-4"
                  >
                    <p className="text-lg">
                      Добре дошли в <strong>Cyber Security Hub</strong> – интерактивна платформа, с която ще
                      практикувате основни умения по кибер сигурност: сканиране на портове, оценка на силата на
                      пароли и проверка на знания чрез куиз.
                    </p>
                    <p>
                      Използвайте бутоните по-горе, за да навигирате през различните функционалности.
                    </p>
                  </motion.div>
                )}
              </AnimatePresence>
            </TabsContent>

            {/* Port Scanner */}
            <TabsContent value="scanner" className="mt-6">
              <AnimatePresence mode="wait">
                {tab === "scanner" && (
                  <motion.div
                    key="scan"
                    variants={fade}
                    initial="hidden"
                    animate="visible"
                    exit="exit"
                    className="space-y-4"
                  >
                    <div className="flex gap-2">
                      <Input
                        placeholder="Въведете IP адрес (симулация)"
                        value={target}
                        onChange={(e) => setTarget(e.target.value)}
                      />
                      <Button onClick={handleScan}>Сканирай</Button>
                    </div>
                    {scanData.length > 0 && (
                      <div className="grid grid-cols-1 lg:grid-cols-2 gap-4">
                        <Card className="p-4">
                          <h3 className="font-semibold mb-2">Резултати</h3>
                          <ul className="space-y-1 max-h-64 overflow-y-auto pr-2">
                            {scanData.map((d) => (
                              <li
                                key={d.port}
                                className={`text-sm px-2 py-1 rounded-lg ${d.status === "open" ? "bg-green-100 text-green-800" : "bg-red-100 text-red-800"}`}
                              >
                                Порт {d.port}: {d.status === "open" ? "отворен" : "затворен"}
                              </li>
                            ))}
                          </ul>
                        </Card>
                        <Card className="p-4">
                          <h3 className="font-semibold mb-2">Графика</h3>
                          <ResponsiveContainer width="100%" height={250}>
                            <BarChart data={scanData.map((d) => ({ name: d.port, value: d.status === "open" ? 1 : 0 }))}>
                              <XAxis dataKey="name" />
                              <YAxis allowDecimals={false} />
                              <Tooltip />
                              <Bar dataKey="value" />
                            </BarChart>
                          </ResponsiveContainer>
                        </Card>
                      </div>
                    )}
                  </motion.div>
                )}
              </AnimatePresence>
            </TabsContent>

            {/* Password Strength */}
            <TabsContent value="password" className="mt-6">
              <AnimatePresence mode="wait">
                {tab === "password" && (
                  <motion.div
                    key="pwd"
                    variants={fade}
                    initial="hidden"
                    animate="visible"
                    exit="exit"
                    className="space-y-4 max-w-md"
                  >
                    <Input
                      type="password"
                      placeholder="Въведете парола"
                      value={pwd}
                      onChange={(e) => setPwd(e.target.value)}
                    />
                    <div className="flex items-center gap-2 text-lg">
                      Сила: <span className="font-bold">{strength.label}</span>
                    </div>
                    <div className="w-full h-4 bg-gray-200 rounded-full overflow-hidden">
                      <div
                        className={`h-full transition-all duration-300 ${
                          strength.score === 0
                            ? "bg-red-500 w-1/5"
                            : strength.score === 1
                            ? "bg-yellow-500 w-2/5"
                            : strength.score === 2
                            ? "bg-blue-500 w-3/5"
                            : "bg-green-600 w-full"
                        }`}
                      ></div>
                    </div>
                  </motion.div>
                )}
              </AnimatePresence>
            </TabsContent>

            {/* Quiz */}
            <TabsContent value="quiz" className="mt-6">
              <AnimatePresence mode="wait">
                {tab === "quiz" && (
                  <motion.div
                    key="quiz"
                    variants={fade}
                    initial="hidden"
                    animate="visible"
                    exit="exit"
                    className="space-y-4 max-w-xl"
                  >
                    {step < questions.length ? (
                      <>
                        <h3 className="text-xl font-semibold">Въпрос {step + 1} от {questions.length}</h3>
                        <p className="mb-4 text-lg">{current.q}</p>
                        <div className="grid grid-cols-1 md:grid-cols-2 gap-2">
                          {current.options.map((opt) => (
                            <Button
                              key={opt}
                              variant={selected === opt ? (opt === current.a ? "success" : "destructive") : "outline"}
                              onClick={() => handleAnswer(opt)}
                              disabled={!!selected}
                            >
                              {opt}
                            </Button>
                          ))}
                        </div>
                        {selected && (
                          <div className="mt-4 flex justify-between items-center">
                            <span className="text-lg font-medium">
                              {selected === current.a ? "Верен отговор!" : `Грешно! Правилен: ${current.a}`}
                            </span>
                            {step < questions.length - 1 && <Button onClick={nextQuestion}>Следващ</Button>}
                            {step === questions.length - 1 && (
                              <Button onClick={nextQuestion}>Резултат</Button>
                            )}
                          </div>
                        )}
                      </>
                    ) : (
                      <div className="text-center space-y-4">
                        <p className="text-2xl font-bold">Вашият резултат: {score} / {questions.length}</p>
                        <Button onClick={() => { setStep(0); setScore(0); }}>Опитай отново</Button>
                      </div>
                    )}
                  </motion.div>
                )}
              </AnimatePresence>
            </TabsContent>
          </Tabs>
        </CardContent>
      </Card>
    </div>
  );
}
