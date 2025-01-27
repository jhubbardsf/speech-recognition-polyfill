## API Report File for "@speechly/speech-recognition-polyfill"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public
export const createSpeechlySpeechRecognition: (appId: string) => SpeechRecognitionClass;

// @public
export const MicrophoneNotAllowedError: SpeechRecognitionErrorEvent;

// @public
export type SpeechEndCallback = () => void;

// @public
export type SpeechErrorCallback = (speechRecognitionErrorEvent: SpeechRecognitionErrorEvent) => void;

// @public
export interface SpeechRecognition {
    abort: () => Promise<void>;
    continuous: boolean;
    interimResults: boolean;
    lang?: string;
    onend: SpeechEndCallback;
    onerror: SpeechErrorCallback;
    onresult: SpeechRecognitionEventCallback;
    onstart: SpeechStartCallback;
    start: () => Promise<void>;
    stop: () => Promise<void>;
}

// @public
interface SpeechRecognitionAlternative_2 {
    confidence: number;
    transcript: string;
}
export { SpeechRecognitionAlternative_2 as SpeechRecognitionAlternative }

// @public
export interface SpeechRecognitionClass {
    new (): SpeechRecognition;
    readonly hasBrowserSupport: boolean;
}

// @public
export interface SpeechRecognitionErrorEvent {
    error: 'not-allowed' | 'audio-capture';
    message: string;
}

// @public
export interface SpeechRecognitionEvent {
    resultIndex: number;
    results: SpeechRecognitionResult_2[];
}

// @public
export type SpeechRecognitionEventCallback = (speechRecognitionEvent: SpeechRecognitionEvent) => void;

// @public
export const SpeechRecognitionFailedError: SpeechRecognitionErrorEvent;

// @public
interface SpeechRecognitionResult_2 {
    0: SpeechRecognitionAlternative_2;
    isFinal: boolean;
}
export { SpeechRecognitionResult_2 as SpeechRecognitionResult }

// @public
export type SpeechStartCallback = () => void;

```
