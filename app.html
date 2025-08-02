<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Master - Interactive High School Math Problems</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.22.5/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            margin: 0;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;

        // Icon components (simplified versions)
        const Calculator = () => <svg className="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 11h.01M12 11h.01M9 11h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z" /></svg>;
        const CheckCircle = () => <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>;
        const XCircle = () => <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>;
        const RotateCcw = () => <svg className="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M3 10h10a8 8 0 018 8v2M3 10l6 6m-6-6l6-6" /></svg>;
        const Trophy = () => <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M20.618 5.984A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" /></svg>;
        const Star = () => <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z" /></svg>;
        const BookOpen = () => <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" /></svg>;
        const ExternalLink = () => <svg className="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" /></svg>;

        const MathProblemApp = () => {
          const [selectedSubject, setSelectedSubject] = useState('algebra');
          const [selectedDifficulty, setSelectedDifficulty] = useState('beginner');
          const [currentProblem, setCurrentProblem] = useState(null);
          const [userAnswer, setUserAnswer] = useState('');
          const [feedback, setFeedback] = useState(null);
          const [score, setScore] = useState({ correct: 0, total: 0 });
          const [showSolution, setShowSolution] = useState(false);
          const [showDocumentation, setShowDocumentation] = useState(false);

          const subjects = {
            algebra: 'Algebra',
            geometry: 'Geometry', 
            trigonometry: 'Trigonometry',
            calculus: 'Calculus'
          };

          const difficulties = {
            beginner: 'Beginner',
            intermediate: 'Intermediate',
            advanced: 'Advanced'
          };

          // Documentation resources for each subject-difficulty combination
          const documentationLinks = {
            algebra: {
              beginner: [
                { title: "Khan Academy - Basic Algebra", url: "https://www.khanacademy.org/math/algebra-basics" },
                { title: "Purplemath - Algebra Lessons", url: "https://www.purplemath.com/modules/index.htm" },
                { title: "Math is Fun - Algebra", url: "https://www.mathsisfun.com/algebra/index.html" }
              ],
              intermediate: [
                { title: "Khan Academy - Algebra I", url: "https://www.khanacademy.org/math/algebra" },
                { title: "Paul's Online Math Notes - Algebra", url: "https://tutorial.math.lamar.edu/Classes/Alg/Alg.aspx" },
                { title: "EdX - Introduction to Algebra", url: "https://www.edx.org/learn/algebra" }
              ],
              advanced: [
                { title: "Khan Academy - Algebra II", url: "https://www.khanacademy.org/math/algebra2" },
                { title: "MIT OpenCourseWare - Algebra", url: "https://ocw.mit.edu/courses/mathematics/" },
                { title: "Wolfram MathWorld - Algebra", url: "https://mathworld.wolfram.com/topics/Algebra.html" }
              ]
            },
            geometry: {
              beginner: [
                { title: "Khan Academy - Basic Geometry", url: "https://www.khanacademy.org/math/basic-geometry" },
                { title: "Math is Fun - Geometry", url: "https://www.mathsisfun.com/geometry/index.html" },
                { title: "CK-12 - Geometry Basics", url: "https://www.ck12.org/geometry/" }
              ],
              intermediate: [
                { title: "Khan Academy - High School Geometry", url: "https://www.khanacademy.org/math/geometry" },
                { title: "Paul's Online Math Notes - Geometry", url: "https://tutorial.math.lamar.edu/Classes/CalcI/CalcI.aspx" },
                { title: "Geometry Textbook Online", url: "https://www.geometrycommon.core.school/" }
              ],
              advanced: [
                { title: "Khan Academy - Advanced Geometry", url: "https://www.khanacademy.org/math/geometry" },
                { title: "Art of Problem Solving - Geometry", url: "https://artofproblemsolving.com/wiki/index.php/Geometry" },
                { title: "Wolfram MathWorld - Geometry", url: "https://mathworld.wolfram.com/topics/Geometry.html" }
              ]
            },
            trigonometry: {
              beginner: [
                { title: "Khan Academy - Intro to Trigonometry", url: "https://www.khanacademy.org/math/trigonometry" },
                { title: "Math is Fun - Trigonometry", url: "https://www.mathsisfun.com/algebra/trigonometry.html" },
                { title: "Purple Math - Trigonometry", url: "https://www.purplemath.com/modules/triggrph.htm" }
              ],
              intermediate: [
                { title: "Khan Academy - Trigonometry", url: "https://www.khanacademy.org/math/trigonometry" },
                { title: "Paul's Online Math Notes - Trig", url: "https://tutorial.math.lamar.edu/Classes/CalcI/TrigFcns.aspx" },
                { title: "SparkNotes - Trigonometry", url: "https://www.sparknotes.com/math/trigonometry/" }
              ],
              advanced: [
                { title: "Khan Academy - Advanced Trigonometry", url: "https://www.khanacademy.org/math/trigonometry" },
                { title: "MIT OpenCourseWare - Trigonometry", url: "https://ocw.mit.edu/courses/mathematics/" },
                { title: "Wolfram MathWorld - Trigonometry", url: "https://mathworld.wolfram.com/topics/Trigonometry.html" }
              ]
            },
            calculus: {
              beginner: [
                { title: "Khan Academy - Differential Calculus", url: "https://www.khanacademy.org/math/differential-calculus" },
                { title: "Paul's Online Math Notes - Calculus I", url: "https://tutorial.math.lamar.edu/Classes/CalcI/CalcI.aspx" },
                { title: "Professor Leonard - Calculus 1", url: "https://www.youtube.com/playlist?list=PLF797E961509B4EB5" }
              ],
              intermediate: [
                { title: "Khan Academy - Integral Calculus", url: "https://www.khanacademy.org/math/integral-calculus" },
                { title: "Paul's Online Math Notes - Calculus II", url: "https://tutorial.math.lamar.edu/Classes/CalcII/CalcII.aspx" },
                { title: "MIT OpenCourseWare - Single Variable Calculus", url: "https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/" }
              ],
              advanced: [
                { title: "Khan Academy - Multivariable Calculus", url: "https://www.khanacademy.org/math/multivariable-calculus" },
                { title: "Paul's Online Math Notes - Calculus III", url: "https://tutorial.math.lamar.edu/Classes/CalcIII/CalcIII.aspx" },
                { title: "MIT OpenCourseWare - Multivariable Calculus", url: "https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/" }
              ]
            }
          };

          const problemBank = {
            algebra: {
              beginner: [
                {
                  question: "Solve for x: 2x + 5 = 13",
                  answer: "4",
                  solution: "2x + 5 = 13\n2x = 13 - 5\n2x = 8\nx = 4",
                  type: "equation"
                },
                {
                  question: "Simplify: 3x + 2x - x",
                  answer: "4x",
                  solution: "3x + 2x - x = (3 + 2 - 1)x = 4x",
                  type: "simplify"
                },
                {
                  question: "If y = 2x + 3, what is y when x = 5?",
                  answer: "13",
                  solution: "y = 2x + 3\ny = 2(5) + 3 = 10 + 3 = 13",
                  type: "substitution"
                }
              ],
              intermediate: [
                {
                  question: "Solve the system: x + y = 7, 2x - y = 5",
                  answer: "x = 4, y = 3",
                  solution: "From equation 1: y = 7 - x\nSubstitute into equation 2:\n2x - (7 - x) = 5\n2x - 7 + x = 5\n3x = 12\nx = 4\ny = 7 - 4 = 3",
                  type: "system"
                },
                {
                  question: "Factor: x² - 5x + 6",
                  answer: "(x - 2)(x - 3)",
                  solution: "Looking for two numbers that multiply to 6 and add to -5\n-2 × -3 = 6 and -2 + (-3) = -5\nSo x² - 5x + 6 = (x - 2)(x - 3)",
                  type: "factoring"
                }
              ],
              advanced: [
                {
                  question: "Solve: x² - 4x + 1 = 0 (use quadratic formula)",
                  answer: "x = 2 ± √3",
                  solution: "Using x = (-b ± √(b² - 4ac)) / 2a\na = 1, b = -4, c = 1\nx = (4 ± √(16 - 4)) / 2 = (4 ± √12) / 2 = (4 ± 2√3) / 2 = 2 ± √3",
                  type: "quadratic"
                }
              ]
            },
            geometry: {
              beginner: [
                {
                  question: "What is the area of a rectangle with length 8 and width 5?",
                  answer: "40",
                  solution: "Area = length × width = 8 × 5 = 40 square units",
                  type: "area"
                },
                {
                  question: "What is the perimeter of a square with side length 6?",
                  answer: "24",
                  solution: "Perimeter = 4 × side length = 4 × 6 = 24 units",
                  type: "perimeter"
                }
              ],
              intermediate: [
                {
                  question: "Find the area of a triangle with base 10 and height 6",
                  answer: "30",
                  solution: "Area = (1/2) × base × height = (1/2) × 10 × 6 = 30 square units",
                  type: "triangle"
                },
                {
                  question: "What is the circumference of a circle with radius 4? (use π ≈ 3.14)",
                  answer: "25.12",
                  solution: "Circumference = 2πr = 2 × 3.14 × 4 = 25.12 units",
                  type: "circle"
                }
              ],
              advanced: [
                {
                  question: "Find the volume of a sphere with radius 3 (use π ≈ 3.14)",
                  answer: "113.04",
                  solution: "Volume = (4/3)πr³ = (4/3) × 3.14 × 3³ = (4/3) × 3.14 × 27 = 113.04 cubic units",
                  type: "sphere"
                }
              ]
            },
            trigonometry: {
              beginner: [
                {
                  question: "What is sin(30°)?",
                  answer: "0.5",
                  solution: "sin(30°) = 1/2 = 0.5\nThis is a special angle in trigonometry",
                  type: "special_angle"
                },
                {
                  question: "What is cos(0°)?",
                  answer: "1",
                  solution: "cos(0°) = 1\nAt 0°, the cosine (adjacent/hypotenuse) equals 1",
                  type: "special_angle"
                }
              ],
              intermediate: [
                {
                  question: "If sin(θ) = 3/5, what is cos(θ)? (θ in first quadrant)",
                  answer: "4/5",
                  solution: "Using Pythagorean identity: sin²(θ) + cos²(θ) = 1\n(3/5)² + cos²(θ) = 1\n9/25 + cos²(θ) = 1\ncos²(θ) = 16/25\ncos(θ) = 4/5 (positive in first quadrant)",
                  type: "identity"
                }
              ],
              advanced: [
                {
                  question: "Solve: 2sin(x) - 1 = 0 for 0° ≤ x ≤ 360°",
                  answer: "x = 30°, 150°",
                  solution: "2sin(x) - 1 = 0\n2sin(x) = 1\nsin(x) = 1/2\nx = 30° or x = 180° - 30° = 150°",
                  type: "equation"
                }
              ]
            },
            calculus: {
              beginner: [
                {
                  question: "Find the derivative of f(x) = 3x²",
                  answer: "6x",
                  solution: "Using the power rule: d/dx(ax^n) = nax^(n-1)\nf'(x) = 3 × 2x^(2-1) = 6x",
                  type: "derivative"
                },
                {
                  question: "What is the limit of (2x + 1) as x approaches 3?",
                  answer: "7",
                  solution: "lim(x→3) (2x + 1) = 2(3) + 1 = 6 + 1 = 7\nSince this is a polynomial, we can substitute directly",
                  type: "limit"
                }
              ],
              intermediate: [
                {
                  question: "Find the derivative of f(x) = x³ - 2x² + 5",
                  answer: "3x² - 4x",
                  solution: "f'(x) = d/dx(x³) - d/dx(2x²) + d/dx(5)\nf'(x) = 3x² - 4x + 0 = 3x² - 4x",
                  type: "derivative"
                }
              ],
              advanced: [
                {
                  question: "Evaluate ∫(2x + 3)dx",
                  answer: "x² + 3x + C",
                  solution: "∫(2x + 3)dx = ∫2x dx + ∫3 dx\n= 2∫x dx + 3∫1 dx\n= 2(x²/2) + 3x + C\n= x² + 3x + C",
                  type: "integral"
                }
              ]
            }
          };

          const generateProblem = () => {
            const problems = problemBank[selectedSubject][selectedDifficulty];
            const randomProblem = problems[Math.floor(Math.random() * problems.length)];
            setCurrentProblem(randomProblem);
            setUserAnswer('');
            setFeedback(null);
            setShowSolution(false);
          };

          const checkAnswer = () => {
            if (!currentProblem || !userAnswer.trim()) return;

            const isCorrect = userAnswer.toLowerCase().trim() === currentProblem.answer.toLowerCase().trim();
            
            setScore(prev => ({
              correct: prev.correct + (isCorrect ? 1 : 0),
              total: prev.total + 1
            }));

            setFeedback({
              correct: isCorrect,
              message: isCorrect ? "Correct! Well done!" : "Not quite right. Try again or view the solution."
            });
          };

          const resetScore = () => {
            setScore({ correct: 0, total: 0 });
          };

          useEffect(() => {
            generateProblem();
          }, [selectedSubject, selectedDifficulty]);

          const accuracyPercentage = score.total > 0 ? Math.round((score.correct / score.total) * 100) : 0;

          return (
            <div className="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 p-4">
              <div className="max-w-4xl mx-auto">
                {/* Header */}
                <div className="text-center mb-8">
                  <div className="flex items-center justify-center gap-2 mb-4">
                    <Calculator className="w-8 h-8 text-blue-600" />
                    <h1 className="text-4xl font-bold text-gray-800">Math Master</h1>
                  </div>
                  <p className="text-gray-600">Interactive High School Math Problems</p>
                </div>

                {/* Controls */}
                <div className="bg-white rounded-xl shadow-lg p-6 mb-6">
                  <div className="grid md:grid-cols-2 gap-4 mb-4">
                    <div>
                      <label className="block text-sm font-medium text-gray-700 mb-2">Subject</label>
                      <select 
                        value={selectedSubject}
                        onChange={(e) => setSelectedSubject(e.target.value)}
                        className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                      >
                        {Object.entries(subjects).map(([key, name]) => (
                          <option key={key} value={key}>{name}</option>
                        ))}
                      </select>
                    </div>
                    <div>
                      <label className="block text-sm font-medium text-gray-700 mb-2">Difficulty</label>
                      <select 
                        value={selectedDifficulty}
                        onChange={(e) => setSelectedDifficulty(e.target.value)}
                        className="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                      >
                        {Object.entries(difficulties).map(([key, name]) => (
                          <option key={key} value={key}>{name}</option>
                        ))}
                      </select>
                    </div>
                  </div>

                  {/* Score Display */}
                  <div className="flex items-center justify-between bg-gray-50 rounded-lg p-4">
                    <div className="flex items-center gap-4">
                      <div className="flex items-center gap-2">
                        <Trophy className="w-5 h-5 text-yellow-500" />
                        <span className="font-medium">Score: {score.correct}/{score.total}</span>
                      </div>
                      {score.total > 0 && (
                        <div className="flex items-center gap-2">
                          <Star className="w-5 h-5 text-blue-500" />
                          <span className="text-sm text-gray-600">Accuracy: {accuracyPercentage}%</span>
                        </div>
                      )}
                    </div>
                    <button
                      onClick={resetScore}
                      className="flex items-center gap-2 px-3 py-1 text-sm text-gray-600 hover:text-gray-800 transition-colors"
                    >
                      <RotateCcw className="w-4 h-4" />
                      Reset
                    </button>
                  </div>
                </div>

                {/* Problem Display */}
                {currentProblem && (
                  <div className="bg-white rounded-xl shadow-lg p-6 mb-6">
                    <div className="mb-6">
                      <div className="flex items-center gap-2 mb-3">
                        <span className="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-medium">
                          {subjects[selectedSubject]} - {difficulties[selectedDifficulty]}
                        </span>
                      </div>
                      <h2 className="text-xl font-semibold text-gray-800 mb-4">
                        {currentProblem.question}
                      </h2>
                      
                      <div className="space-y-4">
                        <input
                          type="text"
                          value={userAnswer}
                          onChange={(e) => setUserAnswer(e.target.value)}
                          placeholder="Enter your answer..."
                          className="w-full p-4 text-lg border-2 border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                          onKeyPress={(e) => e.key === 'Enter' && checkAnswer()}
                        />
                        
                        <div className="flex gap-3 flex-wrap">
                          <button
                            onClick={checkAnswer}
                            disabled={!userAnswer.trim()}
                            className="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 disabled:bg-gray-300 disabled:cursor-not-allowed transition-colors font-medium"
                          >
                            Check Answer
                          </button>
                          <button
                            onClick={generateProblem}
                            className="px-6 py-3 bg-gray-600 text-white rounded-lg hover:bg-gray-700 transition-colors font-medium"
                          >
                            New Problem
                          </button>
                          <button
                            onClick={() => setShowSolution(!showSolution)}
                            className="px-6 py-3 bg-orange-600 text-white rounded-lg hover:bg-orange-700 transition-colors font-medium"
                          >
                            {showSolution ? 'Hide Solution' : 'Show Solution'}
                          </button>
                          <button
                            onClick={() => setShowDocumentation(!showDocumentation)}
                            className="px-6 py-3 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-colors font-medium flex items-center gap-2"
                          >
                            <BookOpen className="w-4 h-4" />
                            {showDocumentation ? 'Hide Resources' : 'Study Resources'}
                          </button>
                        </div>
                      </div>
                    </div>

                    {/* Feedback */}
                    {feedback && (
                      <div className={`flex items-center gap-3 p-4 rounded-lg ${
                        feedback.correct ? 'bg-green-50 text-green-800' : 'bg-red-50 text-red-800'
                      }`}>
                        {feedback.correct ? 
                          <CheckCircle className="w-5 h-5" /> : 
                          <XCircle className="w-5 h-5" />
                        }
                        <span className="font-medium">{feedback.message}</span>
                        {!feedback.correct && (
                          <span className="ml-2 text-sm">
                            Correct answer: <strong>{currentProblem.answer}</strong>
                          </span>
                        )}
                      </div>
                    )}

                    {/* Documentation Links */}
                    {showDocumentation && (
                      <div className="mt-4 p-4 bg-purple-50 border-l-4 border-purple-400 rounded-r-lg">
                        <h3 className="font-semibold text-purple-800 mb-3 flex items-center gap-2">
                          <BookOpen className="w-5 h-5" />
                          Study Resources for {subjects[selectedSubject]} - {difficulties[selectedDifficulty]}
                        </h3>
                        <div className="space-y-2">
                          {documentationLinks[selectedSubject][selectedDifficulty].map((link, index) => (
                            <a
                              key={index}
                              href={link.url}
                              target="_blank"
                              rel="noopener noreferrer"
                              className="flex items-center gap-2 text-purple-700 hover:text-purple-900 hover:underline transition-colors"
                            >
                              <ExternalLink className="w-4 h-4" />
                              {link.title}
                            </a>
                          ))}
                        </div>
                        <p className="text-sm text-purple-600 mt-3 italic">
                          These resources provide additional explanations and practice problems for this topic.
                        </p>
                      </div>
                    )}

                    {/* Solution */}
                    {showSolution && (
                      <div className="mt-4 p-4 bg-yellow-50 border-l-4 border-yellow-400 rounded-r-lg">
                        <h3 className="font-semibold text-yellow-800 mb-2">Solution:</h3>
                        <pre className="text-sm text-yellow-800 whitespace-pre-wrap font-mono">
                          {currentProblem.solution}
                        </pre>
                      </div>
                    )}
                  </div>
                )}

                {/* Footer */}
                <div className="text-center text-gray-500 text-sm">
                  <p>Practice makes perfect! Keep solving problems to improve your math skills.</p>
                </div>
              </div>
            </div>
          );
        };

        ReactDOM.render(<MathProblemApp />, document.getElementById('root'));
    </script>
</body>
</html>
