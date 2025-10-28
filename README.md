# Log_Content
import React from 'react';
import { Database, Cloud, RefreshCw, Zap, Github } from 'lucide-react';

export default function DataPipelineViz() {
  return (
    <div className="w-full h-screen bg-gradient-to-br from-slate-900 to-slate-800 p-8 flex items-center justify-center">
      <div className="w-full max-w-6xl">
        <h1 className="text-3xl font-bold text-white mb-12 text-center">Data Pipeline Architecture</h1>
        
        <div className="relative flex items-center justify-between">
          {/* GitHub Actions Trigger */}
          <div className="flex flex-col items-center z-10">
            <div className="bg-gradient-to-br from-gray-700 to-gray-900 p-6 rounded-lg shadow-2xl border-2 border-gray-500">
              <Github className="w-12 h-12 text-white mb-2" />
              <div className="text-white font-bold text-lg">GitHub</div>
              <div className="text-gray-300 text-lg font-bold">Actions</div>
            </div>
            <div className="mt-2 bg-gray-800 text-gray-300 px-3 py-1 rounded text-sm font-mono">
              Trigger
            </div>
          </div>

          {/* Arrow to Faking */}
          <div className="flex-1 flex items-center mx-4">
            <div className="flex-1 h-1 bg-gradient-to-r from-gray-500 to-purple-500"></div>
            <svg className="w-6 h-6 text-purple-500" fill="currentColor" viewBox="0 0 20 20">
              <path fillRule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clipRule="evenodd" />
            </svg>
          </div>

          {/* Source - Faking */}
          <div className="flex flex-col items-center z-10">
            <div className="bg-gradient-to-br from-purple-500 to-purple-700 p-6 rounded-lg shadow-2xl border-2 border-purple-400">
              <Zap className="w-12 h-12 text-white mb-2" />
              <div className="text-white font-bold text-lg">Faking</div>
              <div className="text-purple-200 text-sm mt-1">Data Source</div>
            </div>
            <div className="mt-2 bg-purple-900 text-purple-200 px-3 py-1 rounded text-sm font-mono">
              10s interval
            </div>
          </div>

          {/* Arrow 1 */}
          <div className="flex-1 flex items-center mx-4">
            <div className="flex-1 h-1 bg-gradient-to-r from-purple-500 to-blue-500"></div>
            <div className="text-blue-400 text-sm font-mono mx-2">10s</div>
            <svg className="w-6 h-6 text-blue-500" fill="currentColor" viewBox="0 0 20 20">
              <path fillRule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clipRule="evenodd" />
            </svg>
          </div>

          {/* Middle Stage - Cassandra & Azure */}
          <div className="flex flex-col items-center gap-4 z-10">
            <div className="bg-gradient-to-br from-blue-500 to-blue-700 p-6 rounded-lg shadow-2xl border-2 border-blue-400">
              <Database className="w-10 h-10 text-white mb-2" />
              <div className="text-white font-bold">Cassandra</div>
            </div>
            <div className="bg-gradient-to-br from-cyan-500 to-cyan-700 p-6 rounded-lg shadow-2xl border-2 border-cyan-400">
              <Cloud className="w-10 h-10 text-white mb-2" />
              <div className="text-white font-bold">Azure</div>
            </div>
          </div>

          {/* Arrow 2 - CDC */}
          <div className="flex-1 flex items-center mx-4">
            <div className="flex-1 h-1 bg-gradient-to-r from-blue-500 to-green-500"></div>
            <div className="text-green-400 text-sm font-semibold mx-2">CDC</div>
            <svg className="w-6 h-6 text-green-500" fill="currentColor" viewBox="0 0 20 20">
              <path fillRule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clipRule="evenodd" />
            </svg>
          </div>

          {/* ETL */}
          <div className="flex flex-col items-center z-10">
            <div className="bg-gradient-to-br from-green-500 to-green-700 p-6 rounded-lg shadow-2xl border-2 border-green-400">
              <RefreshCw className="w-12 h-12 text-white mb-2" />
              <div className="text-white font-bold text-lg">ETL</div>
              <div className="text-green-200 text-sm mt-1">Transform</div>
            </div>
          </div>

          {/* Arrow 3 */}
          <div className="flex-1 flex items-center mx-4">
            <div className="flex-1 h-1 bg-gradient-to-r from-green-500 to-cyan-500"></div>
            <div className="text-cyan-400 text-sm font-semibold mx-2">CDC</div>
            <svg className="w-6 h-6 text-cyan-500" fill="currentColor" viewBox="0 0 20 20">
              <path fillRule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clipRule="evenodd" />
            </svg>
          </div>

          {/* Final Azure */}
          <div className="flex flex-col items-center z-10">
            <div className="bg-gradient-to-br from-cyan-500 to-cyan-700 p-6 rounded-lg shadow-2xl border-2 border-cyan-400">
              <Cloud className="w-12 h-12 text-white mb-2" />
              <div className="text-white font-bold text-lg">Azure</div>
              <div className="text-cyan-200 text-sm mt-1">Destination</div>
            </div>
          </div>
        </div>

        {/* Legend */}
        <div className="mt-12 bg-slate-800 p-6 rounded-lg border border-slate-700">
          <h3 className="text-white font-bold mb-4">Pipeline Flow</h3>
          <div className="grid grid-cols-2 gap-4 text-sm text-slate-300">
            <div>• GitHub Actions triggers the pipeline</div>
            <div>• Faking generates data every 10 seconds</div>
            <div>• Data flows to Cassandra and Azure</div>
            <div>• CDC captures changes from data stores</div>
            <div>• ETL processes and transforms the data</div>
            <div>• Final output stored in Azure destination</div>
          </div>
        </div>
      </div>
    </div>
  );
}
