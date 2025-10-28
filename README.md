Member 3 – Market Indices Component
// --- Member 3 START ---
// File: MarketIndices.jsx
import { MarketChart } from "@/components/MarketChart";
import { BarChart3 } from "lucide-react";

// Mock data for indices
const marketIndices = [
  { name: "NIFTY 50", value: 21850.45, change: 245.3, changePercent: 1.13, trend: "up" },
  { name: "SENSEX", value: 72456.78, change: -89.45, changePercent: -0.12, trend: "down" },
  { name: "MIDCAP", value: 12345.67, change: 156.89, changePercent: 1.29, trend: "up" },
  { name: "BANK NIFTY", value: 48567.23, change: 432.56, changePercent: 0.9, trend: "up" }
];

const MarketIndices = () => {
  return (
    <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
      {marketIndices.map((index) => (
        <MarketChart
          key={index.name}
          indexName={index.name}
          currentValue={index.value}
          change={index.change}
          changePercent={index.changePercent}
          trend={index.trend}
        />
      ))}
    </div>
  );
};

export default MarketIndices;
// --- Member 3 END ---

